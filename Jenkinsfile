#!groovy
node {
	
	stage('Build') { // <2>
		./externalstuff.groovy;
	}
	stage {
		echo "Testing...";
	}
	stage {
		echo "Deploying...";
		emailext body: 'Some information regarding the email.', recipientProviders: [[$class: 'DevelopersRecipientProvider']], subject: 'Hi You\'ve Stated the Pipeline', to: 'machsleep@gmail.com'
	}
}

