pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                script {
                    // Compiling the .cpp file using a shell script
                    sh 'g++ -o my_program hello.cpp'
                }
            }
        }

        stage('Test') {
            steps {
                script {
                    // Printing the output of the compiled .cpp file
                    sh './my_program'
                }
            }
        }

        stage('Deploy') {
            steps {
                echo 'deployed!'
            }
        }
    }

    post {
        failure {
            echo 'Pipeline failed'
        }
    }
}
