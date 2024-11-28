pipeline {
  agent {
    docker {
      image 'fedora:41'
    }

  }
  stages {
    stage('Test') {
      steps {
        sh 'echo "Test pipline"'
      }
    }

    stage('Test multi comand') {
      steps {
        sh '''echo "test comand 1"
echo test "comand 2" echo test "comand 3"'''
      }
    }

    stage('test install update and program') {
      steps {
        sh '''dnf update
dnf install wget'''
      }
    }

  }
}