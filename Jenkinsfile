
pipeline {
  agent any
  stages{
    stage ('Build') {
      steps {
        sh '''
        source ~/unit_test/env/bin/activate
        pipenv install
        '''
      }
    }
    stage ('test') {
      steps {
        sh '''
        py.test --verbose --junit-xml test-reports/results.xml sources/test_calc.py
      }
      post {
        always{
          junit 'test-reports/results.xml'
        }
      }
    } 
  }
}
    























