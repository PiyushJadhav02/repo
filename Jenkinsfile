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
					sh 'kubectl create deployment nginx --image=nginx:latest'
					sh 'kubectl expose deployment nginx --type=NodePort --port=31297'
					sh 'kubectl port-forward svc/nginx 92:8080'
				}
			}
		}
    }
}

