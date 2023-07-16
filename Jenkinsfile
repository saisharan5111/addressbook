pipeline {
  agent any
  parameters {
    string(name: 'Env', defaultValue: 'Test', description: 'version to deploy')
    booleanParam(name:'executeTests', choices: ['1.1', '1.2', '1.3'])
  }

  stages {
    stage('Compile') {
      steps {
        script {
          echo "Compiling the code"
        }
      }
    }

    stage('UnitTest') {
      when {
        expression {
          params.executeTests == true
        }
      }
      steps {
        script {
          echo "Running the test cases"
        }
      }
    }

    stage('Package') {
      steps {
        script {
          echo "Packaging the code"
        }
      }
    }

    stage('Deploy') {
      steps {
        script {
          echo "Deploying the app"
          echo "Deploying to env:${params.Env}"
          echo "Deploying the app version ${params.APPVERSION}"
        }
      }
    }
  }
}
pipeline {
  agent any
  parameters {
    string(name: 'Env', defaultValue: 'Test', description: 'version to deploy')
    booleanParam(name: 'executeTests', defaultValue: true, description: 'decide to run tc')
    choice(name: 'BRANCH', choices: ['1.1', '1.2', '1.3'])
  }
  
  environment {
    NEW_VERSION = '2.1'
  }
  
  stages {
    stage('Compile') {
      steps {
        script {
          echo "Compiling the code"
        }
      }
    }

    stage('UnitTest') {
      when {
        expression {
          params.executeTests == true
        }
      }
      steps {
        script {
          echo "Running the test cases"
        }
      }
    }

    stage('Package') {
      input {
        message "select the version to package"
        ok "Version Selected"
        parameters {
          choice(name: 'NEWAPP', choices: ['1.2', '2.1', '3.1'])
        }
      }
      steps {
        script {
          echo "Packaging the code"
          echo "packaging version ${NEWAPP}"
        }
      }
    }

    stage('Deploy') {
      steps {
        script {
          echo "Deploying the app"
          echo "Deploying to env:${params.Env}"
          echo "Deploying the app Version ${params.APPVERSION}"
        }
      }
    }
  }
}

