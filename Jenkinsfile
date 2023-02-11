pipeline {
      agent any

      tools{
       maven "M2_HOME"

      }
      stages {
            stage('Build Application..') {
                  steps {
                        sh 'mvn clean package'
                    
                  }
            
          post {
              success {
                  echo "starting  the archive process"
                  archiveArtifacts artifacts: '**/*.war'
              }
          }
            }
          
      }
}
