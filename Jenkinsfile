pipeline {
  agent any
  stages {
    stage('git') {
      steps {
        sh 'echo "This is my first blueOcean Pipeline script"'
        git(url: 'https://github.com/omrKalyan/myfirstjenkinsfile', branch: 'main')
      }
    }

    stage('shell') {
      steps {
        sh '''whoami
date
echo $PATH
ls -la'''
      }
    }

    stage('build') {
      steps {
        sh 'sh \'ant -f build.xml -v\''
      }
    }

    stage('artifact') {
      steps {
        archiveArtifacts(artifacts: '/dist/*.jar', fingerprint: true, onlyIfSuccessful: true)
      }
    }

  }
}