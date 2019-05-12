pipeline {
    agent { node {label 'slave10'}}

    stages {
        stage ('Compile Stage') {

            steps {
               
                    sh 'mvn clean compile'
                
            }
        }

        stage ('Testing Stage') {

            steps {
                
                    sh 'mvn test'
                
            }
        }


        stage ('Deployment Stage') {
            steps {
                
                    sh 'mvn package'
                
            }
        }
    }
}
