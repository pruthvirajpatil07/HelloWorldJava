pipeline {
  agent any
  stages {
    stage('Checkout') {
      steps {
        git url: 'https://github.com/pruthvirajpatil07/HelloWorldJava.git', branch: 'main'
      }
    }
    stage('Build') {
      steps {
        sh 'javac HelloWorld.java'
      }
    }
    stage('Run') {
      steps {
        sh 'java HelloWorld'
      }
    }
  }
  post {
    success {
      archiveArtifacts artifacts: '**/*.class', fingerprint: true
    }
    always {
      echo "Pipeline finished"
    }
  }
}
