pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                script {
                    echo "Compiling hello.cpp"
                    sh 'g++ main/hello.cpp -o main/hello_exec'
                }
            }
        }

        stage('Test') {
            steps {
                script {
                    echo "Executing hello_exec"
                    // Introduced an intentional error by changing the filename
                    sh './wrong_file'
                }
            }
        }

        stage('Deploy') {
            steps {
                script {
                    echo "Deployment Stage (Placeholder)"
                }
            }
        }
    }

    post {
        failure {
            echo "Pipeline Failed!"
        }
    }
}
