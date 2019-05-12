pipeline {
    agent any

    stages {
        stage ('Compile Stage') {

            steps {
                withEvn(maven : 'Apache Maven 3.5.2') {
                    sh 'mvn clean compile'
                }
            }
        }

        stage ('Testing Stage') {

            steps {
                withEvn(maven : 'Apache Maven 3.5.2') {
                    sh 'mvn test'
                }
            }
        }


        stage ('Deployment Stage') {
            steps {
                withEvn(maven : 'Apache Maven 3.5.2') {
                    sh 'mvn package'
                }
            }
        }
    }
}
