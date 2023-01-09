pipeline {
      agent any
	  
	  tools{
	      maven "M2_HOME"
		  
		}
		
      stages {
            stage('Build Application') {
                  steps {
                        sh 'mvn clean package'
                    
                  }
            
            post {
			    success {
                    echo "Strating the archive process"
					archiveArtifacts artifacts: '**/*.war'
					
			       }
				   
				}
    		}

               stage('Deploy application') {
                  steps {
                        build job: 'APPLICATION-DEPLOYMENT-JOB'
                    
                  }

		  }		  
          
      }
}
