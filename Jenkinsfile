pipeline {
  agent any
  stages {
    stage('Hello') {
      steps {
        echo 'Hello World'
      }
    }
    stage('advedt') {
      steps {
        echo 'hello again'
      }
    }
    stage('Foo') {
      steps {
        ws(dir: 'test') {
          git 'https://github.com/udacity/create-your-own-adventure'
          sh 'du -sh'
        }
        
      }
    }
    stage('done') {
      steps {
        echo 'Done'
      }
    }
  }
}