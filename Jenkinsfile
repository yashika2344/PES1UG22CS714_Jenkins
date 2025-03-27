pipeline {
    agent any  // Runs on any available agent

    stages {
        stage('Build') {
            steps {
                script {
                    echo "Compiling hello.cpp"
                    sh 'g++ main/hello.cpp -o main/hello_exec'  // Compile C++ file
                }
            }
        }

        stage('Test') {
            steps {
                script {
                    echo "Executing hello_exec"
                    sh './main/hello_exec'  // Run the compiled executable
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
