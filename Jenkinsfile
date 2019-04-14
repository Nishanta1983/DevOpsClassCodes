pipeline{
     agent any
        
	stages {
            stage (Compile) {
		      steps {
		         withMaven(maven : 'maven') {
                         sh 'mvn clean complie'
			     }
              }
	        }

            stage (Test){
              steps {
		        withMaven(maven : 'maven') {
			    sh 'mvn test'
		        }
			  }	 
            }
        
		    stage (Package){
		      steps {
		         withMaven(maven : 'maven') {
		         sh 'mvn package'
		         }
		      }
		    }
			
			stage (Deploy) {
			   steps {
			      withMaven(maven : 'maven') {
				  sh 'mvn deploy'
				  }
			   }	  
			}
	}
}

