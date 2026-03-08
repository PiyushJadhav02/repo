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
		stage{
			container('kubectl'){
				steps{
					sh'kubectl get pods -n jenkins'
				}
			}
		}
    }
}

