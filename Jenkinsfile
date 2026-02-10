pipeline {
    agent {
        label 'k8s-agent'
    }
    stages {
        stage('Test') {
            steps {
                sh 'echo Running on Kubernetes agent'
                sh 'kubectl get pods'
            }
        }
    }
}

