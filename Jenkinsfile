pipeline{
  agent any 
  stages {
    stage('Build') {
      steps {
        build 'PES1UG21CS036-1'
        sh 'cd main \ng++ hello.cpp -o output'
      }
    }
    stage('Test') {
      steps {
        sh './main/outut'
      }
    }
    stage('Deploy') {
      steps {
        echo 'Deployed!!'
      }
    }
  }
    post {
      failure {
        error 'Pipeline failed'
      }
    }
}
