pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo 'Building..'
                jdk = 'C:/Program Files/Java/jdk1.8.0_131'
				  env.JAVA_HOME = "${jdk}"
				
				  echo "jdk installation path is: ${jdk}"
				
				  // next 2 are equivalents
				  bat "${jdk}/bin/java -version"
				
				  // note that simple quote strings are not evaluated by Groovy
				  // substitution is done by shell script using environment
				  bat '$JAVA_HOME/bin/java -version'
                
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