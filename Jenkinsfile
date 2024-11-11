pipeline {
    agent any
    stages {
        stage('this is build stage') {
            steps {
                echo "this is build stage"
            }
        }
        stage ('this is sonar stage') {
            steps {
                echo " this is sonar stage"
            }
        }
        stage ('this is nexus') {
            steps {
                echo " this is nexus stage"
            }
        }
        stage ('this is dev stage') {
            steps {
                echo " this is dev stage"
            }
        }
        stage ('this is stage env') {
            when {
                expression {
                    BRANCH_NAME == /(production|staging)
                }
            }
            steps {
                echo "deployting to stage"
            }
        }
    }
}
