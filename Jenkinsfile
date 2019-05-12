pipeline {
    agent any
      
    stages {
        stage ('Compile Stage') {
            agent { label 'slave10' }

            steps {
               
                    sh 'mvn clean compile'
                
            }
        }

        stage ('Testing Stage') {
            agent { label 'slave10 }

            steps {
                
                    sh 'mvn test'
                
            }
        }


        stage ('Deployment Stage') {
            agent { label 'slave10' }

            steps {
                
                    sh 'mvn package'
                
            }
        }
    }
}
