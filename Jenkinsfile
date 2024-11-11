pipeline {
    agent any
    stages {
        stage ("this is expression condition"){
            when {
                expression{
                    branch_name == /(hotfix|feature)/
                }
            }
            steps {
                echo " deployed to production"
            }
        }
        stage  ("this is general stage") {
            steps {
            echo " this is normal stage"
            }

        }
    }
}
