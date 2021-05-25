pipeline {
    agent any

    stages {
        stage ('Validate Stage') {

            steps {
                withMaven(maven : 'maven_3_6_3') {
                    sh 'mvn clean validate'
                }
            }
        }

        stage ('compile Stage') {

            steps {
                withMaven(maven : 'maven_3_6_3') {
                    sh 'mvn compile'
                }
            }
        }


        stage ('Testing Stage') {
            steps {
                withMaven(maven : 'maven_3_6_3') {
                    sh 'mvn test'
                }
            }
        }
    }
}
