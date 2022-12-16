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
      steps{
        sshagent(credentials: ['APPServerUser']) {
            sh'''
            ls 
            git --version
            '''
        }
      }
    }
  }
}
