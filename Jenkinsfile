properties(
 
 
pipeline {
  agent any
  
  stages {
    stage("Python"){
      steps{
        withPythonEnv("/usr/bin/${params.PYTHON3}") {
          script {
            if ( env.REQUIREMENTS_FILE.isEmpty() ) {
              sh "python3 --version"
              sh "pip --version"
              sh "echo Requirements file not set. Run Python without requirements file."
            }
            else {
              sh "python3 --version"
              sh "pip --version"
              sh "echo Requirements file found. Run PIP install using requirements file."
              withFileParameter('REQUIREMENTS_FILE') {
                sh 'cat $REQUIREMENTS_FILE > requirements.txt'
              }
              sh "pip install -r requirements.txt"
            }
          }
        }
      }
    }
  }
}
