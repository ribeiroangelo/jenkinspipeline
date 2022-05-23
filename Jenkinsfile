pipeline {
    agent {
        docker {
            image 'qnib/pytest' 
        }
    }
    stages{
        stage('Test') {
            steps{
                sh '''
                coverage run --source app/ -m pytest tests/ -s -vv --junit-xml=src/tests/unit_integration_test_results.xml
                coverage html --fail-under=86
                '''
            }
        }
    }
}
