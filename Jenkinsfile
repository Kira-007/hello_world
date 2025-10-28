pipeline{
  agent any

  triggers{
    pollSCM('*/5 * * * *')
  }
  stages{
    stage("Build"){
      steps{
        sh 'sudo docker build -t mydoc:1.0 .'
      }
    }
    stage("Run Container"){
      steps{
        sh 'sudo docker run -d -p80:80 --name test1 mydoc:1.0'
      }
    }
  }
}
