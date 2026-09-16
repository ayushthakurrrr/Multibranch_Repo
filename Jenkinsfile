pipeline {
    agent aws_agent

    stages{
        stage('Build'){
            sh 'echo "Building"'
        }
        stage('Test'){
            sh 'echo "Testing"'
        }
        stage('Append'){
            sh 'echo "appended on $BRANCH_NAME" > file1.txt'
        }
        stage('Deploy'){
            sh 'echo "Deploying"'
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