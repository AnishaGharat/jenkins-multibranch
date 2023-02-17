pipeline {
   agent any
   stages {
       stage('Git checks') {
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

               echo "Deploying Code in main"

               """
          }
      }
   }
}
