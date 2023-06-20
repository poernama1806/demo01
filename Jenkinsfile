pipeline{
    agent any
    environment {
        AWS_ACCESS_KEY_ID='506314646276'
        AWS_DEFAULT_REGION='us-east-1'
        IMAGE_REPO_NAME='myapi'
        IMAGE_TAG='latest'
        REPO_URI='public.ecr.aws/o6v5g0d0'
    }
    stages {
        stage ('Build') {
            steps (
                sh 'aws ecr-public get-login-password --region $(AWS_DEFAULT_REGION) | docker login --username AWS --password-stdin $(REPO_URI)'
            )
        }
    }
}
