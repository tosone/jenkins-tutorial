pipeline {
  agent {
    node {
      label 'alpine'
    }

  }
  stages {
    stage('checkout scm') {
      parallel {
        stage('checkout scm') {
          steps {
            checkout scm
          }
        }

        stage('') {
          steps {
            archiveArtifacts(artifacts: 'README.md', fingerprint: true)
          }
        }

      }
    }

    stage('test') {
      steps {
        container(name: 'alpine') {
          sh 'echo hello-world'
        }

      }
    }

  }
}