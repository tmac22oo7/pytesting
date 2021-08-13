
pipeline {
  agent any
  stages{
    stage ('test') {
       sh ''' 
       python3 -m venv test
       source test/bin/activate
       pip install pytest
       py.test --verbose --junit-xml test-reports/results.xml sources/test_calc.py
       '''
    }
  }
}
    























