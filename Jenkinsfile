pipeline {
  agent any
  stages {
    stage('initialize') {
      agent any
      steps {
        echo 'Staring the Upatch installation'
      }
    }

    stage('Upatch Config File Creation') {
      steps {
        sh 'sh /scratch/create_upatch_config_file.sh'
      }
    }

  }
}