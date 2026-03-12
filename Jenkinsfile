pipeline {
 agent any

 stages {

  stage('Clone Repo') {
   steps {
    git branch: 'main', url: 'https://github.com/ManojKumar8244/devops-ci-cd-pipeline.git'
   }
  }

  stage('Build Docker Image') {
   steps {
    sh 'docker build -t manoj-devops-app .'
   }
  }

  stage('Run Container') {
   steps {
    sh 'docker run -d -p 8081:80 manoj-devops-app'
   }
  }

 }
}
