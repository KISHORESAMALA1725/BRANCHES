// When CONDITION //
pipeline {
    agent {
        label 'java-slave'
    }
    stages {
        stage ('when example'){
            when {
                expression {
                    branch_name ==~ /(feature|hotfix)/
                }
            }
            steps {
                echo "this branch is executed"
            }
        }
    }
}
