pipeline {
  agent any
  
  stages {
    stage('Build') {
      steps {
        sh '/var/jenkins_home/workspace/PES1UG20CS213-1/main/cs213_exec' // compile .cpp file using shell script
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
