pipeline {
    agent any

    stages {
        stage('build') {
            steps {
                sh './mvnw clean install -PbuildDocker'
                sh 'docker-compose up -d'
            }
        }
        stage('test') {
            steps {
                echo 'Testing'
            }
        }
        stage('deploy') {
            steps {
                echo 'Deploying'
            }
        }
    }
    post {
        always {
            cleanWs()
        }
    }
}
