
pipeline{
 agent any
 stages {
 
  stage ('Compile Stage'){
       steps {
       
       withMaven(maven: 'maven3.6.0'){
             sh 'mvn clean package'
	     }
	    }
	  }

   stage ('Tesing Stage'){
        steps {
                 withMaven(maven: 'maven3.6.0') {
		 
		 sh 'mvn test'
		 }
	      }
	  }

  stage ('Deployment Stage'){ 
          steps {
	  
	        withMaven(maven: 'maven3.6.0'){
		         sh 'mvn deploy'
			  }
	         } 
		 
        }
  
    }
  
  
  }
