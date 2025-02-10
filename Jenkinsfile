pipeline {
    agent any
    stages {
      stage('Test') {
        steps {
          println "Hello Pushpa"
          sh '''
            #!/bin/basah
            python3 --version
            python3 prg1.py
          '''
        }
      }
    }
}
