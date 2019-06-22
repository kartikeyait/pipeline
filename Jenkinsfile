node {
   stage('Git_Project download') {
    git 'https://github.com/kartikeyait/Loginapp.git'
     
   }
   stage('Clean') {
	sh 'mvn clean'
    }
	
  stage('Code Scan') {
	sh 'mvn sonar:sonar -Dsonar.host.url=http://34.67.25.19:9000 -Dsonar.login=32d9e7ed5e02252c9a7016b5d1d346aba5926184'
    }
	
   stage('Package') {
	sh 'mvn package'
    }
	
   stage('Deploy') {
	sh 'mvn deploy'
    }
	}
