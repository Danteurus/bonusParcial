pipeline {
    agent any

    tools {
        // Install the Maven version configured as "M3" and add it to the path.
        maven "Maven 3.8.4"
    }

    stages {
        stage('limpiar') {
            steps {
                bat "mvn -Dmaven.test.failure.ignore=true clean"
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