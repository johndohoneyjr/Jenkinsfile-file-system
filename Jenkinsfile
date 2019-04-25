pipeline {   
  agent {
    node {
      label 'master'
    }  
  }
  environment {
       ATLAS_TOKEN      = "${env.ATLAS_TOKEN}"
  }
  stages {

    stage('file-system-demo') {
      steps {
    sh 'touch test.txt'
    sh 'ls ../../../../../'
    sh 'ls /'
    sh 'ls $HOME'
    sh 'ls $JENKINS_HOME'
    sh 'ls $TMPDIR'
    sh '''
        echo $ATLAS_TOKEN
        echo $(pwd)
        ls .
        ls $(pwd)
        rm test.txt
        ls -lag
     '''
      }
    }
  }
}
