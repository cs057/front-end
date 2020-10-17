pipeline {
  agent any
  stages {
    stage('build') {
      steps {
        echo 'this is build job'
        sh 'npm install'
      }
    }

    stage('test') {
      steps {
        echo 'this is test job'
        sh 'npm test'
      }
    }

    stage('package') {
      steps {
        echo 'this is package job'
        sh 'npm run package'
        archiveArtifacts '**distribution/*.zip'
      }
    }

  }
  post {
    always {
      echo 'this pipeline has completed...'
    }

  }
}