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
    agent {
        docker {
            image 'node:7.4'
        }
    }

    steps {
        echo "Branch is ${env.BRANCH_NAME}..."

        withNPM(npmrcConfig:'my-custom-npmrc') {
            echo "Performing npm build..."
            sh 'npm install'
        }
    }
}

  }
}