pipeline {
  agent {
    docker {
      image 'fedora:41fed'
    }

  }
  stages {
    stage('update') {
      agent {
        docker {
          image 'fedora:41'
        }

      }
      steps {
        sh 'dnf update -y'
      }
    }

    stage('wget') {
      agent {
        docker {
          image 'fedora:41'
        }

      }
      steps {
        sh 'dnf install wget'
      }
    }

    stage('download') {
      agent {
        docker {
          image 'fedora:41'
        }

      }
      steps {
        sh 'wget -P /tmp/ https://github.com/Oz73/System_administration/raw/refs/heads/main/rpm/test-bash-1.0-1.fc40.noarch.rpm'
      }
    }

    stage('install') {
      agent {
        docker {
          image 'fedora:41'
        }

      }
      steps {
        sh 'rpm -ivh /tmp/test-bash-1.0-1.fc40.noarch.rpm'
      }
    }

    stage('use script') {
      agent {
        docker {
          image 'fedora:41'
        }

      }
      steps {
        sh 'test_bash.sh'
      }
    }

  }
}