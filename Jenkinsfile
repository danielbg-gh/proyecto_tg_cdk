pipeline {
  agent any
  stages {
    stage('Inicio_Enviroment') {
      steps {
        echo 'Iniciando construccion de proyecto....'
        sh 'env'
      }
    }

    stage('Show-Docker-Env') {
      steps {
        sh 'docker -v'
      }
    }

  }
}