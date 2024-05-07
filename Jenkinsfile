pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        script {
          docker.build("my-hello-world:${env.BUILD_ID}")
        }
      }
    }
    stage('Deploy') {
      steps {
        script {
          kubectl("apply -f k8s-deployment.yaml")
        }
      }
    }
  }
}
