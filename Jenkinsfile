pipeline {
    agent any
    stages {
        stage ('this is first stage') {
            steps {
                echo "this is first stage"
            }
        }
        stage ('this is prod stage'){
            options {
                timeout(time: 30, unit: 'SECONDS')
            }
            input {
                message "Shall we continue ??"
                parameters {
                    string (name: 'USERNAME', defaultValue: 'siva', description: 'Enter your name')
                    text (name: 'ENTER TEXT HERE', defaultValue: 'enter data', description: "enter some data")
                    choice (name: 'PUT SOME CHOICE', choices: 'yes\nno', description: 'enter your choice')
                }
            }
            steps {
                echo "enter name ${USERNAME}"
            }
        }
    }
}
