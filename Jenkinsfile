pipeline {
 agent any

 stages {

  stage('Checkout') {
   steps {
    git 'https://github.com/Bhagyavan8050/tric.git'
   }
  }

  stage('Build Docker Image') {
   steps {
    sh 'docker build -t tric .'
   }
  }

  stage('Run Container') {
   steps {
    sh 'docker run -d -p 80:80 tric'
   }
  }

 }

}
