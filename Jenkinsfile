pipeline {
  agent any
  stages {
    stage('Inicio_Enviroment') {
      steps {
        echo 'Iniciando construccion de proyecto....'
        sh 'env'
      }
    }

    stage('docker Env') {
      steps {
        sh 'docker -v'
      }
    }

    stage('Build') {
      steps {
        sh '''cat versionImage | xargs ./scripts/build.sh
#cat ./scripts/build.sh'''
      }
    }

    stage('Run Container') {
      steps {
        sh 'docker run --name proyapi -itd --rm -p 5000:5000 rogermz/proyectoapi:1.1'
      }
    }

  }
}