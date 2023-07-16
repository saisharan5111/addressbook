pipeline {
    agent any
    parameters{
        string(name:'ENV,defaultValue:'TEST',description:'version to deply to test')
    }
    stages {
        stage('COMPILE') {
            agent any
            steps {
                script{
                    echo "COMPILING THE CODE"
                }
                          }
            }
    }
}

