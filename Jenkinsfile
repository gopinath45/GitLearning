pipeline {
    agent any
    stages {
        stage('Initialization') {
            when {
                  branch 'dev'
              }
            steps {
                echo "${JAVA_HOME}"
                bat "java -version"
                echo "Working on dev branch"
            }
        }
   }
}