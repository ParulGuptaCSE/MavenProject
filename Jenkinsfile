pipeline {
    agent any
    environment {
       PATH = "/Users/parulgupta/Downloads/apache-maven-3.6.3/bin:$PATH"
    } 
    stages {
        stage(‘clone and clean the repo’) { 
            steps {
			
			sh “mvn clean” 
            }
        }
        stage('Test') { 
            steps {
                Sh “mvn test”
            }
        }
        stage('Deploy') { 
            steps {
                Sh “mvn package”
            }
        }
    }
}
