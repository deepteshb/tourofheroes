pipeline {
  agent any
  stages {
    stage('CheckOut') {
      steps {
        git(url: 'https://github.com/deepteshb/tourofheroes.git', branch: 'master', credentialsId: 'deepteshgithub')
      }
    }

    stage('Build') {
      steps {
        npm(command: 'npm install', workspaceSubdirectory: '/var/jenkins/nodejs')
      }
    }

  }
}