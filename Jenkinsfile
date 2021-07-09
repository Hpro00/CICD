pipeline {
    
    agent any
    environment {
        Version = 'v2207'
    }
    stages {
        stage("build") {
            steps {
                echo "Start Building GoD..."
                echo "Building Version: ${Version}"
            }
        }
        stage("test") {
            steps {
                echo "Start Testing GoD..."
                echo "Testing Version: ${Version}"
            }
        }
        stage("deploy") {
            steps {
                echo "Start Deploying GoD..."
                echo "Deploying Version: ${Version}"
            }
        }
    }
    post {
        success {
            echo "Congratulation!"
        }
        failure {
            echo "Something went wrong!"
        }
    }
}
