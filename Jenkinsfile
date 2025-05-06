pipeline {
    agent any

    stages {
        stage('Klooni repo') {
            steps {
                git branch: 'main', url: 'https://github.com/Aleksandra-Semjonova/test.git'
                // Asenda ülalolev link oma GitHub repo URL-iga
            }
        }

        stage('Paigalda sõltuvused') {
            steps {
                sh 'npm install'
            }
        }

        stage('Käivita rakendus') {
            steps {
                sh 'nohup npm start &'
                echo 'Rakendus käivitatud!'
            }
        }
    }
}
