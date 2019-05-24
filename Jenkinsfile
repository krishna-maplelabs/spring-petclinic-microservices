pipeline {
    agent any

    stages {
        stage('build') {
            sh './mvnw clean install -PbuildDocker'
            sh 'docker-compose up -d'
        }
        stage('test') {
            echo 'Testing'
        }
        stage('deploy') {
            echo 'Deploying'
        }
    }
    post {
        always {
            cleanWs()
        }
    }
}