pipeline  {
    agent any

    stages {
        stage('Build Image') {
            steps {
                sh 'docker build -t nextjscicd:latest .'
            }
        }
        stage('Deploy') {
            steps {
                sh 'docker run -d -p 4334:3000 nextjscicd:latest'
            }
        }
    }
}