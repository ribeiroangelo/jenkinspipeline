pipeline {
    agent {
        docker {
            image 'qnib/pytest' 
        }
    }
    stage('Test') {
        steps{
            sh 'python -m pytest src --verbose --junit-xml test-reports/results.xml'
        }
    }
}
