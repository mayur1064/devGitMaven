pipeline {
    agent any
    tools {
        maven 'maven_home'
    }

    stages {
        
        stage ('Initialize') {
            steps {
                bat '''
                    echo "PATH = ${PATH}"
                    echo "maven_ = ${M2_HOME}"
                '''
            }
        }
        
        
         stage ('Build') {
            steps {
                bat 'mvn clean package' 
            }
         }

        stage ('Testing Stage') {

            steps {
                    bat 'mvn test'
                
            }
        }


        
    }
}
