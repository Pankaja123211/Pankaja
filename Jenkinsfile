pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        echo 'Building'
        sh 'jenkins/build.sh'
      }
    }
    stage('Test') {
      steps {
        echo 'Testing'
        sh 'jenkins/test-all.sh'
        junit 'target/**/*.xml'
      }
    }
    stage('Deploy') {
      steps {
        echo 'Deploying'
        sh 'jenkins/deploy.sh'
      }
    }
  }
}