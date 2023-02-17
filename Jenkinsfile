pipeline {
   agent any
   parameters {
        string(name: "TEST_STRING", defaultValue: "ssbostan", trim: true, description: "Sample string parameter")
    }
   stages {
       stage('Git checks') {
           steps {
                script{
                    echo env.BRANCH_NAME
                    def files = getChangedFilesList()
                    echo "${files}"
                    echo "$params.TEST_STRING"
                }
              
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

// returns a list of changed files
@NonCPS
String getChangedFilesList() {
    changedFiles = []
    for (changeLogSet in currentBuild.changeSets) {
        for (entry in changeLogSet.getItems()) { // for each commit in the detected changes
            for (file in entry.getAffectedFiles()) {
                changedFiles.add(file.getParent()) // add changed file to list
            }
        }
    }
    return changedFiles
}