#!groovy

node {
	stage('Build') { // <2>
		parallel linuxBuild: {
			node("linux") {
				echo "Building linux";
			}
		},
		node("windows") {
			echo "Building windows";
		}
	}
	stage('Test') {
		echo "Testing...";
	}
	stage('Deploy') {
		echo "Deploying...";
		emailext body: 'Some information regarding the email.', recipientProviders: [[$class: 'DevelopersRecipientProvider']], subject: 'Hi You\'ve Stated the Pipeline', to: 'machsleep@gmail.com'
	}
}
