// PARALLEL //
pipeline {
    agent {
        label 'java-slave'
    }
    environment {
        branch = "production"
    }
    stages {
        stage ('this is maven stage'){
            steps {
                echo "this is maven stage"
            }
        }
        stage ('this is sonar stage'){
            steps {
                echo "this is sonar stage"
            }
        } 
        stage ('THIS IS PARALLEL STAGE') {
            parallel {
                stage ('this is scan stage') {
                    steps {
                        echo "this is scan stage"
                    }
                }
                stage ('this is fortify stage') {{}
                    steps {
                        echo "this is fortify stage"
                    }
                }
                stage ('this is bucket stage') {
                    steps {
                        echo "this is bucket stage"
                    }
                }
            }
        }      
    }
}
