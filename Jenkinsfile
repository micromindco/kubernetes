pipeline {
  agent any
  stages {
    stage('S1') {
      parallel {
        stage('S1') {
          steps {
            sh '''yum install docker -y 
service docker start'''
          }
        }
        stage('S12') {
          steps {
            node(label: 'Nodeone')
          }
        }
      }
    }
    stage('S2') {
      steps {
        sh 'docker pull centos'
      }
    }
  }
}