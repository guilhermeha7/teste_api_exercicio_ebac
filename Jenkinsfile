pipeline {
    agent any

    stages {
        stage('Clonar o repositório') {
            steps {
                git branch: 'main', url: 'https://github.com/guilhermeha7/teste_api_exercicio_ebac'
            }
        }

        stage('Instalar dependência') {
            steps {
                bat 'npm install'
            }
        }

        stage('Executar testes') {
            steps {
               bat 'set NO_COLOR=1 && npm run cy:run'
            }
        }
    }
}