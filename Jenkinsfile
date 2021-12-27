pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                echo 'building the application'  
                echo 'Application built' 
            }
        }

        stage('test') {
            steps {
                echo 'testing the application'   
            }
        }

        stage('deploy') {
            steps {
                echo 'deploying the application'   
                withCredentials([
                    usernamePassword(credentials:'my-app-pipeline', usernameVariable: USER, passwordVariable: PASSWORD)
                ]){
                    echo "some script ${USER} ${PWD}"
                }
            }
        }
    }
}