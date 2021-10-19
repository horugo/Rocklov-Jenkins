pipeline {
    agent {
        docker { image 'python' }
    }

    stages {
        stage('Preparation'){
            steps{
                sh 'pip install -r requirements.txt'
            }
        }
        stage('Run API Ttestes') {
            steps {
                sh 'cd backend && robot -d ./logs tests'
            }
        }
        stage('Run  UI Tests'){
            steps{
                sh 'cd frontend && robot -d ./logs tests'
            }
        }
    }
}