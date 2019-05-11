pipeline {
    agent any

    stages {
        stage ('Clean Stage') {

            steps {
                withMaven(maven : 'maven-3.5.2') {
                    sh 'mvn clean '
                }
            }
        }

        stage ('Testing Stage') {

            steps {
                withMaven(maven : 'maven-3.5.2') {
                    sh 'mvn test'
                }
            }
        }


        stage ('Deployment Stage') {
            steps {
                withMaven(maven : 'maven-3.5.2') {
                    sh 'mvn package'
                }
            }
        }
    }
}
