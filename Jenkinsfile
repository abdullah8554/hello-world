// Powered by Infostretch 

timestamps {

node () {

	stage ('jenkins coversion to pipeline - Checkout') {
 	 checkout([$class: 'GitSCM', branches: [[name: '*/master']], doGenerateSubmoduleConfigurations: false, extensions: [], submoduleCfg: [], userRemoteConfigs: [[credentialsId: '9abfaed0-bbc4-49b4-b90a-56de7437fa4b', url: 'https://github.com/abdullah8554/hello-world.git']]]) 
	}
	stage ('jenkins coversion to pipeline - Build') {
 			// Maven build step
	withMaven(maven: 'mvn') { 
 			if(isUnix()) {
 				sh "mvn clean install package " 
			} else { 
 				bat "mvn clean install package " 
			} 
 		} 
	}
}
}