//docker login//
pipeline {
    agent {
        label 'docker-slave'
    }
    environment {
        DOCKER_CREDS = credentials('DOCKER_CREDS')
    }
    stages {
        stage ('Push to docker hub') {
            steps {
                echo "***** DOCKER IMAGES *****"
                sh "docker images"
                echo "***** DOCKER REMOVE IMAGES *****"
                // sh "docker container remove ${docker ps -aq}"
                sh "docker rmi ${docker images}"       
                echo "***** DOCKER PULL IMAGES *****"
                sh "docker pull devopswithcloudhub/nginx:green"
                echo "***** DOCKER INFO IMAGES *****"
                sh "docker images"   
                echo "***** DOCKER RE-TAG IMAGES *****"            
                sh "docker tag devopswithcloudhub/nginx:green kishoresamala1725/nginx:green"
                echo "***** DOCKER HUB LOGIN *****"                                                       
                sh "docker login -u ${DOCKER_CREDS_USR} -p ${DOCKER_CREDS_PSW}"
                echo "***** DOCKER PUSH IMAGES *****"  
                sh "docker image push kishoresamala1725/nginx:green"             
            }
        }
    }
}
