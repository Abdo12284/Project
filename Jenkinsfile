pipeline {
    agent any  // Any available Jenkins agent will run the job.
    stages {
        stage('Build') {
            steps {
                script {
                    dockerImage = docker.build("myapp")  // Build the Docker image from the Dockerfile
                }
            }
        }
        stage('Test') {
            steps {
                sh 'echo "Running tests..."'  // Placeholder for actual tests
            }
        }
        stage('Deploy') {
            steps {
                script {
                    dockerImage.push("my-dockerhub-repo/myapp")  // Push Docker image to Docker Hub (or private registry)
                }
            }
        }
    }
}
