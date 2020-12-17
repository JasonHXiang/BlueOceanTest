pipeline {
  agent any
  stages {
    stage('Hello') {
      parallel {
        stage('Hello') {
          steps {
            echo 'Hello World'
          }
        }

        stage('jasonStep1') {
          steps {
            sh '''cd /root/env3/
source bin/activate
python -m rich.progress'''
            sh 'echo "step1-1"'
          }
        }

        stage('jasonStep2') {
          steps {
            sh '''sleep 30s
echo "step2"'''
          }
        }

      }
    }

    stage('Stage02') {
      parallel {
        stage('Stage02') {
          steps {
            sh 'echo "Stage02 Step1"'
          }
        }

        stage('stage02-2') {
          steps {
            sh '''sleep 20s
echo "Stage02-2"'''
          }
        }

      }
    }

    stage('EndStage') {
      steps {
        sh '''sleep 5s
echo "End"'''
      }
    }

  }
}