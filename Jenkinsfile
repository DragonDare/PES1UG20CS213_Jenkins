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
        sh './cs213.exec' // print output of .cpp file using shell script
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
