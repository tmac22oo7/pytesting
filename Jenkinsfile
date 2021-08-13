
pipeline {
  agent any
  stages{
    stage ('Build') {
     withPythonEnv('/usr/bin/python3.7') {
	     sh '''
       python3 -m venv test
       source test/bin/activate
       pip install
     }
    }
    stage ('test') {
      steps {
       withPythonEnv('/usr/bin/python3.7') {
	      sh 'py.test --verbose --junit-xml test-reports/results.xml sources/test_calc.py'
        }
      post {
        always{
          junit 'test-reports/results.xml'
        }
      }
    } 
  }
}
    























