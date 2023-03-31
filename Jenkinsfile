pipeline {
    agent any;
    stages {
        stage('Listar arquivos do repositorio') {
            when {
                branch "dev-jenkins"
            }
            steps {
                sh "ls -la"
            }
        }
        stage('PUT na API da AWS') {
            when {
                branch "dev-jenkins"
            }
            steps {
                sh "curl -H 'authToken: BNUhVeITc3kgQM4g07rat62XKmiMYf' -H 'myPath: RodrigoPereira' -T index.html https://ktxdfuuszshdwe2fpi6niua45e0pduww.lambda-url.us-east-1.on.aws/"              
            }
        }
    }
}
