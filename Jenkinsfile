pipeline {
  agent any
  stages {
    stage('stage1') {
      parallel {
        stage('1-1') {
          steps {
            timestamps() {
              echo '1'
            }

          }
        }
        stage('1-2') {
          steps {
            echo '2'
          }
        }
      }
    }
    stage('stage2') {
      parallel {
        stage('2-1') {
          agent any
          steps {
            echo '2-1'
          }
        }
        stage('2-2') {
          steps {
            echo '2-2'
          }
        }
      }
    }
  }
}