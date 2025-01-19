pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                sh './mvnw clean install'
            }
        }
        stage('Run Application') {
            steps {
                sh 'java -jar target/nome-do-seu-projeto.jar'
            }
        }
    }
    post {
        success {
            echo 'Build e execução bem-sucedidos!'
        }
        failure {
            echo 'Erro na execução do pipeline.'
        }
    }
}
