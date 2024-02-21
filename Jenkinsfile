pipeline {
  agent any
  tools { 
        maven 'Maven_3_5_2'  
    }
   stages{
    stage('CompileandRunSonarAnalysis') {
            steps {	
		sh 'mvn clean verify sonar:sonar -Dsonar.projectKey=buggywebappdevsecops -Dsonar.organization=buggywebappdevsecops -Dsonar.host.url=https://sonarcloud.io -Dsonar.token=4db57578f06c010671863104a6e5f5651f520772'
			}
        } 
  }
}
