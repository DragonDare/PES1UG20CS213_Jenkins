pipeline {
  agent any
  
  stages {
    stage('Build') {
      steps {
        sh 'g++ /var/jenkins_home/workspace/PES1UG20CS213-1/cs213_5.cpp -o scrip' // compile .cpp file using shell script
      }
    }
    
    stage('Test') {
      steps {
        sh './scriptsss' // Should fail since object file name is scrip, not scriptsss
      }
    }
    
    stage('Deploy') {
      steps {
        echo 'Deployment successful'
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
