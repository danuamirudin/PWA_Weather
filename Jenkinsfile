pipeline {
    agent any 

    stages {
        stage('checkout') {
            agent any 
            steps {
                chekout scm
            }
        }

         stage ('clean') {
            agent any
            steps {
                sh 'rm -rf /var/www/html/pwa/tugas'
            }
        }

        stage('verification') {
            agent any
            steps {
                sh 'ls /var/www/html/pwa'
            }
        }
        stage ('Deploy') {
            agent any
            steps {
                sh 'mv /var/lib/jenkins/workspace/tugas/* /var/www/html/pwa/'
            }
        }
    }
}
