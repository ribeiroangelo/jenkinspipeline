pipeline {
    agent { docker { image 'python:3.10.1-alpine' } }
    stages {
        stage('build') {
            steps {
                sh 'pip3 install pytest --user'
                sh 'python -m pytest src --verbose --junit-xml test-reports/results.xml'
            }
        }
    }
}
