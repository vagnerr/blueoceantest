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
        parallel(
          "advedt": {
            echo 'hello again'
            echo 'ggggg'
            echo 'ggsdgsgd'
            
          },
          "": {
            echo 'Foobar'
            
          }
        )
      }
    }
    stage('Foo') {
      steps {
        ws(dir: 'test') {
          git 'https://github.com/udacity/create-your-own-adventure'
          sh 'du -sh'
        }
        
        input(message: 'We are pausing', id: '1', ok: 'Go for it')
      }
    }
    stage('done') {
      steps {
        echo 'Done'
      }
    }
  }
}