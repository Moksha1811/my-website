pipeline {
    agent any
    stages {
        stage('Clone Repository') {
            steps {
                git url: 'https://github.com/Moksha1811/my-website.git',
                branch: 'main'
            }
        }
        stage('Verify Files') {
            steps {
                sh 'ls -la'
                sh 'cat index.html'
            }
        }
        stage('Deploy Website') {
            steps {
                sh 'mkdir -p/var/www/html'
                sh 'cp index.html /var/www/html/index.html'
                echo 'Website deployed successfully!'
            }
        }
    }
        post {
            success {
                echo 'Pipeline completed! Website is live.'
            }
            failure {
                echo 'Pipeline failed. Check the logs.'
            }
        }
    }
}
