
pipeline {
  agent any
  stages{
    stage ('test') {
       sh 'python3 -m venv test'
       sh 'source test/bin/activate'
       sh 'pip install pytest'
       sh 'py.test --verbose --junit-xml test-reports/results.xml sources/test_calc.py'
       
    }
  }
}
    























