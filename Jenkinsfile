
pipeline {
  agent any
  stages { 
    stage ('build') {
      steps {
       sh '''#!/bin/bash
       python3 -m venv test3
       source test3/bin/activate
       pip install pip --upgrade
       pip install pytest
       '''
      }
    }
    stage ('test') {
      steps {
        sh 'py.test --verbose --junit-xml test-reports/results.xml sources/test_calc.py'
      }
      post {
        always {
          junit 'test-reports/results.xml'
        }
      }
    }
  }
}
    






















