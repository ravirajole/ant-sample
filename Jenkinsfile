pipeline
{
 agent any
 stages
 {
  stage('scm checkout') 
  { steps { git 'https://github.com/ravirajole/gradle-simple.git'}  }

  stage('build the code') {    //build the job clean workspace skip test scripts
   steps { withGradle
	    { sh 'gradle build'} }  
  }
 }
}