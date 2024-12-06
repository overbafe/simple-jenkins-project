pipeline {
    agent any

    stages {
        stage('Clone Repository') {
            steps {
                // Клонирование репозитория
                checkout scm
            }
        }
        stage('Install Dependencies') {
            steps {
                // Установка зависимостей
                sh 'pip install -r requirements.txt'
            }
        }
        stage('Run Script') {
            steps {
                // Запуск скрипта
                sh 'python3 main.py'
            }
        }
    }

    post {
        always {
            echo 'Pipeline execution finished!'
        }
    }
}
