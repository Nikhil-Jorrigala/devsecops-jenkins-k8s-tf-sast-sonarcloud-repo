pipeline {
  agent any
  tools { 
        maven 'Maven_3_5_2'  
    }
   stages{
    stage('CompileandRunSonarAnalysis') {
            steps {	
		sh 'mvn clean verify sonar:sonar -Dsonar.projectKey=devsecopsbuggywebapp01_devsecopsbuggywebapp01 -Dsonar.organization=devsecopsbuggywebapp01 -Dsonar.host.url=https://sonarcloud.io -Dsonar.token=4db57578f06c010671863104a6e5f5651f520772'
			}
        } 
  }
}
