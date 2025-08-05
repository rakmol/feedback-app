pipeline {
  agent any

  environment {
    KUBECONFIG = credentials('kubeconfig')
  }

  stages {
    stage('Checkout Code') {
      steps {
        git 'https://github.com/rakmol/feedback-app.git'
      }
    }

    stage('Deploy to Kubernetes') {
      steps {
        sh 'kubectl apply -f k8s/'
      }
    }
  }
}
