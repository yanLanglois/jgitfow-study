pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo 'Building..'
				bat 'C:/Users/LANGLOIY/Documents/applications/apache-maven-3.5.0/bin/mvn clean install -Dmaven.test.skip=true'
            }
        }
        stage('Test') {
            steps {
                echo 'Testing..'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying....'
            }
        }
    }
}