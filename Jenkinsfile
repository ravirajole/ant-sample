pipeline
{
 agent any
 stages
 {
  stage('scm checkout') 
  { steps { git 'https://github.com/ravirajole/ant-sample.git'}  }

  stage('build the code') {  agent { label 'JAVA'}   //build the job clean workspace skip test scripts
   steps { withAnt(jdk: 'JDK_Home') { 
	    { sh 'mvn clean -B -DskipTests package'} }  
  }
 }
}