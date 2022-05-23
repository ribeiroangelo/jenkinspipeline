pipeline {
    agent { docker { image 'python:3.10.1-alpine' } }
    stages {
        stage('build') {
            steps {
                sh 'python -m pytest src --verbose --junit-xml test-reports/results.xml'
            }
        }
    }
}
