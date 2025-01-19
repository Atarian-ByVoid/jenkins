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
                sh 'java -jar target/demo-0.0.1-SNAPSHOT.jar'
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
