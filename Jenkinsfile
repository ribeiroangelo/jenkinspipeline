pipeline {
    agent {
        node {
            label 'my_local_server'
            customWorkspace '/projects/'
        }
    }
    stages {
        stage('Install Dependencies') {
          steps {
            sh """
              python -m venv .env
              source ./.env/bin/activate
              python -m pip install -r requirements.txt
              python -m pip install pytest pytest-cov coverage
              """
          }
        }
    }
}
