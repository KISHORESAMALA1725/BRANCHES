pipeline {
    agent any
    parameters {
        string (name: 'ENTER NAME', defaultValue: 'SIVA', description: 'Enter your value')
        choice (name: 'Enter_value', choices: ['spscores','spsodsvcp'], description: 'enter value')
    }
    stages {
        stage ('this is stage example') {
            when {
                expression {
                    params.Enter_value == "spscores"
                }   
            }
            steps {
                echo " ******* SPSCORES EXECUTED *******"
            }
        }
        stage ('this is second stage'){
            when {
                expression {
                    params.Enter_value == "spsodsvcp"
                }
            }
            steps {
                echo " ####### SPSODSVCP EXECUTED #######"
            }  
        }    
      
    }
}
