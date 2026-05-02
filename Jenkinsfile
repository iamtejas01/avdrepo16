pipeline {
    agent any

    environment {
        PYTHON = "C:\\Users\\Tejas\\AppData\\Local\\Programs\\Python\\Python314\\python.exe"
    }

    stages {
        stage('Install Dependencies') {
            steps {
                bat '"%PYTHON%" -m pip install --upgrade pip'
                bat '"%PYTHON%" -m pip install --upgrade pandas python-dateutil pytz numpy'
            }
        }

        stage('Show Python Version') {
            steps {
                bat '"%PYTHON%" --version'
                bat '"%PYTHON%" -m pip --version'
            }
        }

        stage('Test Pandas') {
            steps {
                bat '"%PYTHON%" -c "import pandas as pd; print(pd.__version__)"'
            }
        }

        stage('Run extract.py') {
            steps {
                bat '"%PYTHON%" extract.py'
            }
        }
    }
}