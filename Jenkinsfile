pipeline {
    agent any
    stages {
        stage ('This is build-stage'){
            steps {
                echo "this is build stage"
            }
        }
        stage ('THIS IS PRODUCTION STAGE'){
            options {
                timeout (time: 45, unit: 'SECONDS')
            }
            input {
                message "shall we continue ??"
                parameters {
                    string(name: 'NAME', defaultValue: 'SIVA', description: 'ENTER YOUR NAME')
                    choice(name: 'YOUR_CHOICE', choices: ['spscores','spsodsvcp'], description: 'choose one value')
                }
            }
            stage ('this is after input'){
            when {
                expression {
                    params.your_choice == "spscores"
                }
            }
            steps {
                echo " SPSCORES is executed"
            }
            }

        }
    }
}
