pipeline {
    agent any
    tools {
        maven 'maven_home'
    }

    stages {
        
        stage ('Initialize') {
            steps {
                sh '''
                    echo "PATH = ${PATH}"
                    echo "maven_ = ${M2_HOME}"
                '''
            }
        }
        
        
         stage ('Build') {
            steps {
                sh 'mvn clean package' 
            }
         }

        stage ('Testing Stage') {

            steps {
                    sh 'mvn test'
                
            }
        }


        stage ('Deployment Stage') {
            steps {
                    sh 'mvn deploy'
                
            }
        }
    }
}
