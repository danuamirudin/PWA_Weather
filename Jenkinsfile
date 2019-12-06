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
                sh 'mv PWA_Weather /var/www/html/pwa'
            }
        }
    }
}
