pipeline {
    agent any

    environment {
        PYTHON = "C:\\Users\\Tejas\\AppData\\Local\\Programs\\Python\\Python314\\python.exe"
    }

    stages {
        stage('Checkout Code') {
            steps {
                checkout scm
            }
        }

        stage('Install Dependencies') {
            steps {
                bat '"%PYTHON%" -m pip install --upgrade pandas python-dateutil pytz numpy'
            }
        }

        stage('Show Python Version') {
            steps {
                bat '"%PYTHON%" --version'
            }
        }

        stage('Run extract.py') {
            steps {
                bat '"%PYTHON%" extract.py'
            }
        }
    }
}