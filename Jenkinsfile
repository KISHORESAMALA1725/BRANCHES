pipeline {
    agent any
    stages {
        stage ('this is first stage'){
            when {
                expression {
                    branch_name ==~ /(feature|hotfix)/
                }
                steps {
                    echo "this branch is executed"
                }
            }
        }
    }
}
