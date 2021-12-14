pipeline {
    agent any

    tools {
        // Install the Maven version configured as "M3" and add it to the path.
        maven "maven 3.8.4"
    }

    stages {
        stage('compile') {
            steps {
                bat "mvn -Dmaven.test.failure.ignore=true test"
            }
        }

        stage('compile') {
            steps {
                bat "mvn -Dmaven.test.failure.ignore=true compile"
            }
        }

        stage('empacar') {
            steps {
                bat "mvn -Dmaven.test.failure.ignore=true package"
            }
        }
    }
}