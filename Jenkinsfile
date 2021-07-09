pipeline {
    
    agent any
    parameters { 
        choice(name: 'VERSION',choices: ['v2.7', 'v7.5', 'v5.2', 'v2.0', 'v0.1'], descrition: 'Xiu')
        booleanParam(name: 'Test', defaultValue: true, description: 'Make it Simple')    
    }
    tools {
        maven
        jdk
        gradle
    }    
    environment {
        Author = 'BoHieu'
    }
    stages {
        stage("build") {
            steps {
                echo "Start Building GoD..."
                echo "Building Version: ${params.VERSION}"
                echo "Author: ${Author}"
            }
        }
        stage("test") {
            when {
               BRANCH_NAME == 'Hpro00-patch-1'   
                expression {
                    params.Test
                }
            }    
            steps {
                echo "Start Testing GoD..."
                echo "Testing Version: ${params.VERSION}"
                echo "Author: ${Author}"
            }
        }
        stage("deploy") {
            steps {
                echo "Start Deploying GoD..."
                echo "Deploying Version: ${params.VERSION}"
                echo "Author: ${Author}"
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
        alưays {
            echo "Completed Job!"   
        }
    }
}
