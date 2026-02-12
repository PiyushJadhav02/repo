pipeline {
    agent {
        label 'k8s-agent'
    }
    stages {
        stage('Test') {
            steps {
                sh 'echo Running on Kubernetes agent'
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

