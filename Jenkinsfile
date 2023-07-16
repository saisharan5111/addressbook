pipeline {
    agent any
//    tools{
//        jdk 'myjava'
//        maven 'mymaven'
//    }
 //    environment{
 //       IMAGE_NAME='devopstrainer/java-mvn-privaterepos:$BUILD_NUMBER'
 //       DEV_SERVER_IP='ec2-user@52.66.240.173'
 //       APP_NAME='java-mvn-app'
 //   }
    stages {
        stage('COMPILE') {
            agent any
            steps {
                script{
                    echo "COMPILING THE CODE"
                }
                          }
            }
        stage('UNITTEST'){
            agent any
            steps {
                script{
                    echo "RUNNING THE UNIT TEST CASES"
                }
             
            }
        
            }
        stage('PACKAGE+BUILD DOCKER IMAGE ON BUILD SERVER'){
            agent any
                     echo "PACKAGING THE CODE"
        }
