pipeline {
    agent any 

    stages {
        stage('Build Assets') {
            agent any 
            steps {
                echo 'Building Assets...'
            }
        }
        stage('Test') {
            agent any
            steps {
                echo 'Testing stuff...'
            }
        }
        stage ('Deploy') {
            agent any
            steps {
                sh 'mv /var/lib/jenkins/workspace/tugas /var/www/html/pwa'
            }
        }
    }
}
