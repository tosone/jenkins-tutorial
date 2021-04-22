pipeline {
  agent {
    node {
      label 'alpine'
    }
  }

  // environment {
  //   DOCKER_CREDENTIAL_ID = 'dockerhub-id'
  //   GITHUB_CREDENTIAL_ID = 'github-id'
  //   KUBECONFIG_CREDENTIAL_ID = 'demo-kubeconfig'
  //   REGISTRY = 'docker.io'
  //   DOCKERHUB_NAMESPACE = 'docker_username'
  //   GITHUB_ACCOUNT = 'kubesphere'
  //   APP_NAME = 'devops-java-sample'
  // }

  stages {
    stage ('checkout scm') {
      steps {
        checkout(scm)
      }
    }

    stage ('test') {
      steps {
        container ('alpine') {
          sh 'echo hello-world'
        }
      }
    }
  }
}
