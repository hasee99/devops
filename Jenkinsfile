pipeline {
    agent any
    stages {
        stage('check out') {
            steps {
              checkout scm
            }
        }
         stage('Build Image') {
            steps {
              sh 'docker build -t ubunim:latest.'
            }
        }
         stage('Tag Image') {
           
            steps {
               sh 'docker tag ubun.im:latest hasee658/ubun:latest'
            }
        }
         stage('Push Image') {
          
            steps {
               sh 'docker login -u syed0071 -p hasee658#'
                sh 'docker push ubun.im:latest'
            }
        }
    }
    post { 
        aborted { 
            echo 'ABORTED'
        }
         success { 
            echo 'SUCCESS'
        }
         failure { 
            echo 'FAILURE'
        }
        changed { 
            echo 'FAILURE'
        }
    }
    
}

    
    
    
    


