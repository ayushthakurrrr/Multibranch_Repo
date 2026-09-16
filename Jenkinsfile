pipeline {
    agent none

    stages{
        stage('Build'){
            agent any
            steps{
                sh 'echo "Building"'
            }
        }
        stage('Test'){
            agent aws_agent
            steps{
                sh 'echo "Testing"'
            }
        }
        stage('Append'){
            agent any
            steps{
                sh 'echo "appended on $BRANCH_NAME" > file1.txt'
            }
        }
        stage('Deploy'){
            agent any
            steps{
                sh 'echo "Deploying"'
            }
        }
    }

    post{
        always{
            sh 'echo "Exection done"'
        }
        success{
            sh 'echo "Success"'
        }
        failure{
            sh 'echo "Failure"'
        }
    }
}