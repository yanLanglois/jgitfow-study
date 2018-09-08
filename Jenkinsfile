pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo 'Building..'
                bat 'C:/Users/LANGLOIY/Documents/applications/apache-maven-3.5.0/bin/mvn clean compile -Dmaven.test.skip=true'
            }
        }
        stage('Test') {
            steps {
                echo 'Testing..'
                bat 'C:/Users/LANGLOIY/Documents/applications/apache-maven-3.5.0/bin/mvn test'
            }
        }
        stage('Deploy') {
            steps {
                bat 'C:/Users/LANGLOIY/Documents/applications/apache-maven-3.5.0/bin/mvn deploy -Dmaven.test.skip=true'
            }
        }
    }
}