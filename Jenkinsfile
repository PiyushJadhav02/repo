pipeline {
    agent {
    	kubernetes{
        	label 'my-jenkins-jenkins-agent'
		defaultContainer 'kubectl'
	}
    }
    stages {
        stage('Test') {
            steps {
                sh 'echo Running'
				sh 'whoami'
				sh 'hostname'
            }
        }
		stage('Kubectl'){
			steps{
				container('kubectl'){
					sh 'kubectl get pods -n jenkins'
				}
			}
		}
    }
}

