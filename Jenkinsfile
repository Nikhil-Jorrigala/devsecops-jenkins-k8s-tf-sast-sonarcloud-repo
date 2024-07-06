pipeline {
  agent any
  tools { 
        maven 'Maven_3_5_2'  
    }
   stages{
    stage('CompileandRunSonarAnalysis') {
            steps {	
		sh 'mvn clean verify sonar:sonar -Dsonar.projectKey=buggywebappdevsecops -Dsonar.organization=buggywebappdevsecops -Dsonar.host.url=https://sonarcloud.io -Dsonar.token=8d505a38ece950002da7e92bdb41672a5549fd70'
			}
        } 
	   stage('RunSCAAnalysisUsingSnyk') {
            steps {		
				withCredentials([string(credentialsId: 'SNYK_TOKEN', variable: 'SNYK_TOKEN')]) {
					sh 'mvn snyk:test -fn'
				}
			}
    }	
  }
}
