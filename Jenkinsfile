// when not //
pipeline {
    agent {
        label 'java-label'
    }
    environment {
        DEP_TO: "production"
    }
    stages {
        stage ('this is when not example') {
            when {
                not {
                    environment name: "DEP_TO", value: "production"
                }
            }
            steps {
                echo "When not is successfull"
            }
        }
    }
}
