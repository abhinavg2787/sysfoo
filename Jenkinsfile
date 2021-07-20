pipeline {
  agent any
  stages {
    stage('build') {
      steps {
        echo '******** Compiling *******'
        sh 'mvn compile'
      }
    }

    stage('test') {
      steps {
        echo '****** Running Unit tests *******'
        sh 'mvn clean test'
      }
    }
  }
  tools {
    maven 'Maven 3.6.1'
  }
  post {
    always {
      echo 'This pipeline is completed..'
    }

  }
}
