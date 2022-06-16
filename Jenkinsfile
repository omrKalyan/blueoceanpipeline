pipeline {
  agent any
  stages {
    stage('shell') {
      steps {
        sh 'echo "This is a new multi branch pipe"'
      }
    }

    stage('build') {
      steps {
        git(url: 'https://github.com/omrKalyan/myfirstjenkinsfile', branch: 'main')
      }
    }

    stage('buildxml') {
      steps {
        sh 'ant -f build.xml -v'
      }
    }

  }
}