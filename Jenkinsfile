pipeline {
    agent any
  
    stages (
        stage("Build') {
            steps {
              build 'PES22UG21CS586-1'
              sh 'g++ main.cpp-o output'
            } 
        }
        stage('Test') {
            steps {
                sh'./output'
              
            }
        }
        stage('Deploy') {
            steps {
              echo 'Deployed!'
            }
          }
      }
              
      post {
          failure {
               error 'Pipeline Failed
          }
      }
    
  }  
              
