pipeline {
   agent any
   stages {
       stage('Build Code') {
           steps {
               echo "env.BRANCH_NAME"
           }
       }
      stage('Deploy Code') {
          steps {
               sh """
               echo "Deploying Code"
               """
          }
      }
   }
}
