pipeline {
     parameters {
          string(name: 'branch_name', defaultValue: 'master', description: 'Please enter the branch name')
    }
    agent any
    stages {
        stage ('Build'){
            when {
                  branch 'dev'
            }
              steps {
                 echo "Working on dev branch"
                }
        }
    }

}