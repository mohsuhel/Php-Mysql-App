pipeline {
    agent any
    stages {
        stage('clean workspace') {
            steps {
                cleanWs()
            }
        }
        stage('Checkout from Git') {
            steps {
                git branch: 'master', url: 'https://github.com/mohsuhel/Php-Mysql-App.git'
            }
        }
     
        stage("Docker Build & Push") {
            steps {
                script {
                    sh "docker build -t mdsuh/php-mysql:latest ."
                    withCredentials([string(credentialsId: 'dockerHub', variable: 'dockerHub')]) {
                        sh 'docker login -u mdsuh -p $dockerHub'
                        sh "docker push mdsuh/php-mysql:latest "
                    }
                }
            }
        }
        
        stage('Deploy to container'){
          steps{
            sh 'docker run -itd --name php-mysql -p 8081:80 mdsuh/php-mysql:latest'
          }
      }
    }
}
