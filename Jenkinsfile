pipleline{
  agent any
  stages{
     stage('checkout'){
       steps{
         checkout scm
       }
     }
    stage("build"){
          steps{
            echo 'checking python application
            bat 'python -m py_compile app.py'
          }
          }
          stage('test'){
            steps{
              echo 'executing automated tests'
              bat 'python -m unittest app'
            }
          }
          stage('run application'){
            steps {
              bat 'python app.py'
            }
          }
          }
          post {
            success {
              echo 'ci pipleline completed successfully'
            }
            failure {
              echo 'ci pipeline failed'
            }
          }
          }
          
          
      
          
