pipeline {
    agent any 

    stages {
        stage('start') {
            agent any 
            steps {
                echo 'BISMILLAH'
            }
        }

         stage ('clean') {
            agent any
            steps {
                parallel (
                    'clean dir' : {sh 'rm -rf /var/www/html/pwa/*'},
                    'make dir'  : {sh 'mkdir /var/www/html/pwa/'}                
                )
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
