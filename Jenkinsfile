pipeline {
     agent any
        stages {
            stage ('Compile stage') {
		 steps {
		    withMaven(maven : 'MyMaven') {
                    sh 'mvn clean complie'
	            }
		 }
	     }

            stage ('Test stage') {
                 steps {
		    withMaven(maven : 'MyMaven') {
	            sh 'mvn test'
		    }
	          }	 
              }
        
            stage ('Package stage') {
		      steps {
		         withMaven(maven : 'MyMaven') {
		         sh 'mvn package'
		         }
		      }
	      }
			
	     stage ('Deploy stage') {
			   steps {
			      withMaven(maven : 'MyMaven') {
			      sh 'mvn deploy'
			      }
			   }	  
	     }
	}
}

