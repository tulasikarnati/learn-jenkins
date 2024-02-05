pipeline {
    agent {
        node {
            label 'AGENT-1'
        }
}
    environment {
        GREETING = "Good Morning"
    }
    options {
        timeout(time: 1, unit: 'HOURS')
        disableConcurrentBuilds() 
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
                    echo $GREETING
                    sleep 10
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