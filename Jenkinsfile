pipeline {
  agent {
    label 'redhat-family'
  }
  stages {
    stage('Build') {
      post {
        success {
          sh 'echo Funciona'
        }

      }
      steps {
        git 'https://github.com/jafernandez73/blue-pipe-test'
        container(name: 'centos') {
          sh 'yum --version'
          sh ''' echo 1
                echo 2
                echo 3
                '''
        }

      }
    }

    stage('Test') {
      steps {
        sh 'echo Soy un test'
      }
    }

  }
}
