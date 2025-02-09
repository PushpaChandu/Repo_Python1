pipeline {
    agent any
agent {

    docker {

      image 'python:3.5.1'

    }

  }
 
    stages {
        stage('version') { 
            steps {
                
                sh 'python3 --version'
            }
        }
      stage('Hello Test1') { 
            steps {
                sh prg1.sh
                sh python3 prg1.py
            }
        }
    }
}
