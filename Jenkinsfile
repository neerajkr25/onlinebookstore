pipeline {
  agent any
  stages {
    stage('code collect') {
      steps {
        git(url: 'https://github.com/neerajkr25/onlinebookstore.git', branch: 'J2EE', poll: true)
      }
    }

    stage('compile') {
      steps {
        sh 'mvn compile'
      }
    }

    stage('test') {
      steps {
        sh 'mvn clean'
      }
    }

    stage('validate') {
      steps {
        sh 'mvn validate'
      }
    }

    stage('package') {
      steps {
        sh 'mvn package'
      }
    }

  }
}