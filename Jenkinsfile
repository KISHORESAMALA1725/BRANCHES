// anyOf condition
pipeline {
    agent any 
        environment {
            branch = spscorep
        }
        stages {
            stage ('this is any off stage') {
                when {
                    anyOf{
                        expression {
                            branch_name ==~ /(spscorep|spsodsvcp)/
                        }
                        environment name: branch, value: spscorep
                    }
                }
                steps {
                    echo "this spscorep *** spsodsvcp branch are successfull"
                }
            }
        }
    }
