#!groovy

stage('Build') { // <2>
	parallel linuxBuild: {
		node {
			echo "Building linux";
		}
	},
	node("windows") {
		echo "Building windows";
	}
}
stage {
	echo "Testing...";
}
stage {
	echo "Deploying...";
	emailext body: 'Some information regarding the email.', recipientProviders: [[$class: 'DevelopersRecipientProvider']], subject: 'Hi You\'ve Stated the Pipeline', to: 'machsleep@gmail.com'
}

