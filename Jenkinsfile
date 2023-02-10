pipeline {
   agent any
   stages {
       stage('Build Code') {
           steps {
               echo env.BRANCH_NAME
           }
       }
      stage('Deploy Code') {
         when {
                branch 'main'
         }
          steps {
               sh """
               echo "Deploying Code"
               """
          }
      }
   }
}
