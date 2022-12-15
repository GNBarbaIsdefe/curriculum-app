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

    stage('Front-End Unit Test') {
      parallel {
        stage('Front-End Unit Test') {
          steps {
            sh 'cd curriculum-front && npm i && npm run test:unit'
          }
        }

        stage('Checks') {
          steps {
            sh '''echo "DIRECTORIO\\
-----------------------\\
-----------------------";
pwd;
echo "USUARIO\\
-----------------------\\
-----------------------";
echo $USER;
echo "SUBDIRECTORIOS\\
-----------------------\\
-----------------------";
ll'''
          }
        }

      }
    }

  }
}