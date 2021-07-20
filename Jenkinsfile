pipeline {
  agent any
  
  tools{
    maven 'Maven 3.6.1'
  }

  stages{
      stage("build"){
          steps{
              echo '******** Compiling *******'
              sh 'mvn complie'
          }
      }
      stage("test"){
          steps{
              echo '****** Running Unit tests *******'
              sh 'mnv clean test'
          }
      }
      stage("package"){
          steps{
              echo '******* Generating the artifact *******'
              sh 'mvn package -DskipTests'
          }
      }
  }

  post{
    always{
        echo 'This pipeline is completed..'
    }
  }
}
