pipeline {
    agent any    
    stages {        
        stage('Compile') {
            steps {
                // Execute Maven to compile your code
                // You might need to customize the Maven goals depending on your project structure
                sh 'mvn compile'
            }
        }
        
        stage('Test') {
            steps {
                // Execute Maven to run tests
                sh 'mvn test'
            }
        }
        
        stage('Package') {
            steps {
                // Execute Maven to create a deployable package (e.g., JAR, WAR)
                sh 'mvn package'
            }
        }
    }
}
