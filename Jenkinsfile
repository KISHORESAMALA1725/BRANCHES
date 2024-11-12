// anyOf condition //
pipeline {
    agent {
        label 'java-slave'
    }
    environment {
        DEP_TO = "production"
    }
    stages {
        stage ('This is anyOf condition') {
            when {
                anyOf{
                    expression {
                        branch_name ==~ /(spscorep|spsodsvcp)/
                    }
                    environment name: "DEP_TO", value: "production1"
                }
            }
            steps {
                echo "any off condition is successfull"
            }
        }
    }
}
