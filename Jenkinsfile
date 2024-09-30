pipeline
{
 agent any
 stages
 {
  stage('scm checkout') 
  { steps { git 'https://github.com/ravirajole/ant-sample.git'}  }

  stage('build the code') {  agent { label 'JAVA'}   //build the job clean workspace skip test scripts
   steps { withMaven(globalMavenSettingsConfig: '', jdk: 'JDK_Home', maven: 'MVN_home', mavenSettingsConfig: '', traceability: true) 
	    { sh 'mvn clean -B -DskipTests package'} }  
  }
 }
}