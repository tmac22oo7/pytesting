
pipeline {
 agent {
        docker { image 'python:3' }
    }
  stages { 
    stage ('test') {
      steps {
       sh '''
       pip install pip --upgrade
       pip install pytest
       '''
      }
    }
  }
}
    






















