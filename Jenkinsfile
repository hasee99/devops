pipeline {
     agent any
    options {
        // Timeout counter starts AFTER agent is allocated
        timeout(time: 10, unit: 'SECONDS')

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
                echo 'Deploying....'
            }
        }
    }
}
