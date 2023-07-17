pipeline {
    agent any
    parameters{
        string(name:'Env',defaultValue:'Test',description:'version to deply to test')
        booleanParam(name:'executeTests',defaultValue:true,description:'deecide to run tc')
        choice(name:'APPVERSION',choices:['1.1','1.2','1.3'])
            }
    stages {
        stage('COMPILE') {
            steps {
                script{
                    echo "COMPILING THE CODE ${params.APPVERSION}"
                    sh "mvn compile"
                }
            }
        }
    stages {
        stage('TEST') {
            steps {
                script{
                    sh "mvn test"
                }
            }
        }
    stages {
        stage('TEST') {
            steps {
                script{
                    sh "mvn package"
                }
                          }
            }
    }
}
