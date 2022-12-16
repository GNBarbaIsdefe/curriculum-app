pipeline {
  agent {
    node {
      label 'linux'
    }

  }
  stages {
    stage('Checkout Code') {
      steps {
        git(url: 'https://github.com/GNBarbaIsdefe/curriculum-app', branch: 'main')
      }
    }
    stage(credentials: ['Deploy APP']) {
      steps{
        sshagent(['APPServerUser']) {
            sh"ll"
        }
      }
    }
  }
}
