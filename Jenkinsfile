pipeline {
     parameters {
          string(name: 'branch_name', defaultValue: 'master', description: 'Please enter the branch name')
          choice(choices: ['PROD','DEV','TEST'], description: 'Please select environment', name: 'Environment')
          text(name: 'Description', description: 'Please enter details about the project', defaultValue: '')
          booleanParam(name: 'Toggle', defaultValue: true, description: 'Toggle this value')
          string(name: 'node', defaultValue: 'pop', description: 'Select the node')
     }
     agent {
          node {
               label params.node
          }
     }

     stages {
          stage ('Checkout'){
               steps {
                    script {
                         try {
                              
                              git branch: "${params.branch_name}",
                              url: 'https://github.com/gopinath45/GitLearning.git'
                              sh 'pwd;ls'
                    
                         }
                         catch (Exception error) {
                              echo "Error code : ${error}"
                              currentBuild.result = 'FAILURE'
                         }
          
                    }
                    

               }
          }
     }
     
}