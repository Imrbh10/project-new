pipeline{
    agent any
    stages{
        stage('checkout'){
            steps{
                deleteDir()
                sh '''
                git clone https://github.com/Imrbh10/jenkins-deploy.git
                ls -1
                '''
            }
        }
        stage('deploy'){
         steps{
            sh '''
             rm -rf /var/www/html/*
             cp -r jenkins-deploy/* /var/www/html
             '''   
        }
        }
    }
}
