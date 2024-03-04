pipeline{
  agent any 
  stages {
    stage('Build') {
      steps {
        script{
        build 'PES1UG21CS036-1'
        sh 'g++ main.cpp -o output'
        }
      }
    }
    stage('Test') {
      steps {
        sh './output'
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
