pipeline {
    agent aws_agent

    stages{
        stage('Build'){
            steps{
                sh 'echo "Building"'
            }
        }
        stage('Test'){
            steps{
                sh 'echo "Testing"'
            }
        }
        stage('Append'){
            steps{
                sh 'echo "appended on $BRANCH_NAME" > file1.txt'
            }
        }
        stage('Deploy'){
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