pipeline {
    agent {
        docker {
            image 'qnib/pytest' 
        }
    }
    stages{
        stage('Test') {
            steps{
                sh 'python -m pytest src --verbose --junit-xml test-reports/results.xml'
            }
        }
    }
}
