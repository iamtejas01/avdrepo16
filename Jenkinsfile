pipeline {
    agent any
    environment {
        PYTHON = "C:\\Users\\Tejas\\AppData\\Local\\Programs\\Python\\Python314\\python.exe"
    }
    stages {
        stage ('Checkout Code') {
            steps {
                checkout scm
            }

        }
        stage ('Show Python Version') {
            steps {
                bat "${env.PYTHON} --version"
            } 
        }
        stage ('Run extract.py') {
            steps {
                bat "${env.PYTHON} extract.py"
            }         
        }
    }
}