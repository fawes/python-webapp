pipeline {
  agent any
  stages {
    stage('Checkout') {
      steps {
        checkout scm
      }
    }
    stage('Build')  {
      steps {
        sh 'pip install -r requirements.txt'
      }
    }
    stage('Deploy') {
      steps {
        sh 'echo "Deploying the app.."'
        sh 'nohup python app.py &' #bgrun
