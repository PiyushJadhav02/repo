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
	stage('Kubectl'){
		steps{
			container('kubectl'){
				sh 'whoami'
				sh 'kubectl version --client'
				sh 'kubectl get pods'
			}
		}
	}
    }
}

