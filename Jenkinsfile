pipeline{
    agent any
    stages{
        stage('Clone'){
            steps{
                git url: 'https://github.com/KaranManhas22/6weeks_ravina_PYTHON_backend.git', branch: 'main'
            }
        }
        stage('docker build'){
            steps{
                sh 'docker build -t ravinabackend .'
            }
        }
        stage("validation"){
      steps{
        sh 'docker stop backend-container || true'
        sh 'docker rm backend-container || true'
    }
  }
        stage('docker Run'){
            steps{
                sh 'docker run -d --name backend-container -p 8000:8000 ravinabackend'
            }
        }
    }
}

