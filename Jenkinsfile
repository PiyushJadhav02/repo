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
				sh 'kubectl get pods'
			}
		}
	}
    }
}

