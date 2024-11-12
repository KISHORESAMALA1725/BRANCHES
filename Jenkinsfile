// allOf condition //
pipeline {
    agent any
    environment {
        dep_to = "prodcution"
    }
    stages {
        stage ('this is allOf condition') {
            when {
                allOf {
                    environment name: "dep_to", value: "production"
                }
                expression {
                    branch_name ==~ /(spscorep|spsodsvcp)/
                }
            }
            steps{
                echo "this allOf condition is successfull"
            }
        }
    }
}
