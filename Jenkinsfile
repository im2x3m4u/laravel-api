pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                git 'https://github.com/im2x3m4u/laravel-api.git'
                sh 'composer install'
                sh 'cp .env.example .env'
                sh 'php artisan key:generate'
            }
        }
        stage('Test') {
            steps {
                sh './vendor/bin/phpunit'
            }
        }
    }
}
