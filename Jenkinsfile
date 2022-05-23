pipeline {
    agent {
        docker {
            image 'qnib/pytest' 
        }
    }
    stages{
        stage('Test') {
            steps{
                sh 'python -m pytest tests/'
            }
        }
    }
}
