pipeline {
    agent none

    stages{
        stage('Build'){
            agent any
            sh 'echo "Building"'
        }
        stage('Test'){
            agent aws_agent
            sh 'echo "Testing"'
        }
        stage('Append'){
            agent any
            sh 'echo "appended on $BRANCH_NAME" > file1.txt'
        }
        stage('Deploy'){
            agent any
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