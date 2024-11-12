//when environment //
pipeline {
    agent {
        label 'java-slave'
    }
    environment {
        DEPLOY_TO = "PRODUCTION"
    }
    stages {
        stage('this is first stage') {
            when {
                // expression {
                    environment name: "DEPLOY_TO", value: "PRODUCTION"
                // }
            }
            steps {
                echo "PRODCUTION CODE DEPLOYED"

            }
        }
    }
}
