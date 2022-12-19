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

    stage('Deploy APP') {
      steps {
        sshagent(credentials: ['SSHAPP']) {
          sh 'ssh -o StrictHostKeyChecking=no -l userapp 10.67.33.250 uname -a && ls'
        }

      }
    }

  }
}