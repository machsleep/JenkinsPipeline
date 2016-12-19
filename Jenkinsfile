#!groovy
node { // <1>
    stage('Build') { // <2>
        echo "Building...";
    }
    stage('Test') {
        echo "Testing...";
    }
    stage('Deploy') {
        echo "Deploying...";
	emailext body: 'Some information regarding the email.', recipientProviders: [[$class: 'DevelopersRecipientProvider']], subject: 'Hi You\'ve Stated the Pipeline', to: 'machsleep@gmail.com'
    }
}
