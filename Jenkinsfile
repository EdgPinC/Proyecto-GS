pipeline {
    agent any

    tools {
        python 'Python 3' // Defínelo desde Manage Jenkins > Global Tool Configuration
    }

    stages {
        stage('Build') {
            steps {
                echo 'Instalando dependencias...'
                sh 'pip install -r requirements.txt'
            }
        }
        stage('Test') {
            steps {
                echo 'Ejecutando pruebas unitarias...'
                sh 'pytest tests/'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Simulando despliegue...'
                sh 'echo "Desplegando app..."'
            }
        }
    }

    post {
        always {
            echo 'Pipeline terminado'
        }
    }
}
