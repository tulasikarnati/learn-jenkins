pipeline {
    agent {
        node {
            label 'AGENT-1'
        }
}
    environment {
        GREETING = "Good Morning"
    }
    // build
    stages {
        stage('Build') {
            steps {
                echo 'Building..'
            }
        }
        stage('Test') {
            steps {
                echo 'Testing..'
            }
        }
        stage('Deploy') {
            steps {
                sh """
                    echo ""heello shellscript
                    env
                """
            }
        }
    }
    // post build
    post {
        always {
           echo "always run till pipeline runs " 
        }
        failure {
            echo "pipeline is failed"
        }
        success {
            echo "pipeline is success"
        }
    }
}