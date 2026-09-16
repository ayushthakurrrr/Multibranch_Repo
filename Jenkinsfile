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
            agent {
                label "aws_agent"
            }
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
            echo "Exection done"
        }
        success{
            echo "Success"
        }
        failure{
            echo "Failure"
        }
    }
}