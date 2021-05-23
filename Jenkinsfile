pipeline {
  agent any
  tools {nodejs "nodejs"}
  stages {
    stage('CheckOut') {
      steps {
        git(url: 'https://github.com/deepteshb/tourofheroes.git', branch: 'master', credentialsId: 'deepteshgithub')
      }
    }
   stage('npm-build') {
     steps {
        sh 'npm build'
      }
  }
}