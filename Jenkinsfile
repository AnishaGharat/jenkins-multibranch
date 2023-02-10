pipeline {
   agent any
   stages {
       stage('Test Code') {
           steps {
               echo env.BRANCH_NAME
           }
       }
      stage('Deploy Code') {
            when {
                branch 'master'
            }
            steps {
               sh """
               echo "Deploying Code"
               """
          }
      }
   }
}
