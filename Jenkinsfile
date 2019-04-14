pipeline {
     agent any
        stages {
            stage ('Compile stage') {
		 steps {
		    withMaven(maven : 'maven') {
                    sh 'mvn clean complie'
	            }
		 }
	     }

            stage ('Test stage') {
                 steps {
		    withMaven(maven : 'maven') {
	            sh 'mvn test'
		    }
	          }	 
              }
        
            stage ('Package stage') {
		      steps {
		         withMaven(maven : 'maven') {
		         sh 'mvn package'
		         }
		      }
	      }
			
	     stage ('Deploy stage') {
			   steps {
			      withMaven(maven : 'maven') {
			      sh 'mvn deploy'
			      }
			   }	  
	     }
	}
}

