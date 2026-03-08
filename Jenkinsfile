pipeline {
    agent {
    	kubernetes{
        	label 'k8s-agent'
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
    }
}

