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
            ssh -o StrictHostKeyChecking=no userapp@10.67.34.250
            ls 
            git --version
            '''
        }
      }
    }
  }
}
