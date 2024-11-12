// TAG for STAGING //
pipeline {
    agent {
        label 'java-slave'
    }
    environment {
        dep_to = "production"
    }
    stages {
        stage ('this is build stage') {
            steps {
                echo "build stage"
            }
        }
        stage ('this is sonar stage') {
            steps {
                echo "sonar-stage"
            }
        }
        stage ('this is nexus stage') {
            steps {
                echo "nexus-stage"
            }
        }
        stage ('this is STAGE-ENV'){
            when {
                tag pattern: "V\\d{1,2}.\\d{1,2}.\\d{1,2}", comparator: "REGEXP"
            }
            steps {
                echo "Deployed to STAGE-ENV"

            }
        }        
    }
}
