pipeline{
    agent any
    stages{
        stage('Clone'){
            steps{
                git url: 'https://github.com/KaranManhas22/6weeks_ravina_PYTHON_backend.git', branch: 'main', credentialsId: 'new'
            }
        }
        stage('docker build'){
            steps{
                sh 'docker build -t ravinabackend .'
            }
        }
        stage('docker Run'){
            steps{
                sh 'docker run -d -p 8000:8000 ravinabackend'
            }
        }
    }
}
