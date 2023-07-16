pipeline {
    agent any
    parameters{
        string(name:'Env',defaultValue:'Test',description:'version to deply to test')
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

