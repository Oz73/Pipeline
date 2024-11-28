pipeline {
  agent {
    docker {
      image 'fedora:41'
    }

  }
  stages {
    stage('update') {
      steps {
        sh 'dnf update -y'
      }
    }

    stage('wget') {
      steps {
        sh 'dnf install wget'
      }
    }

    stage('download') {
      steps {
        sh 'wget -P /tmp/ https://github.com/Oz73/System_administration/raw/refs/heads/main/rpm/test-bash-1.0-1.fc40.noarch.rpm'
      }
    }

    stage('install') {
      steps {
        sh 'rpm -ivh /tmp/test-bash-1.0-1.fc40.noarch.rpm'
      }
    }

    stage('use script') {
      steps {
        sh 'test_bash.sh'
      }
    }

  }
}