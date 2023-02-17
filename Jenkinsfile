pipeline {
  agent any
  
  stages {
    stage('Build') {
      steps {
        sh 'mvn clean install'
        sh 'g++ -o script cs213_5.cpp' // compile .cpp file using shell script
      }
    }
    
    stage('Test') {
      steps {
        sh './script' // print output of .cpp file using shell script
      }
    }
    
    stage('Deploy') {
      steps {
        // deploy code to production environment
      }
    }
  }
  
  post {
    always {
      script {
        if (currentBuild.result != 'SUCCESS') {
          echo 'pipeline failed'
        }
      }
    }
  }
}
