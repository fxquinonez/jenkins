pipeline {
    agent any

    stages {
        stage('docker build') {
            steps {
                script {
                    sh "docker build -f jenkins/Dockerfile -t fxquinonez/homer_page:1.0.0-${BUILD_ID} jenkins"
                }
            }
        }
        stage('docker push') {
            steps {
                script {
                    sh "docker push fxquinonez/homer_page:1.0.0-${BUILD_ID}"
                }
            }
        }
    }
}