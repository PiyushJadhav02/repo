pipeline {
    agent any
    stages {
        stage('Test') {
            steps {
                sh 'echo Running'
				sh 'whoami'
				sh 'hostname'
				sh 'systemctl status jenkins'
            }
        }
    }
}

