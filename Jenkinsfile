
stage('Init data') {
  sh 'ls'
  sh 'pwd'
}

node('TestNode') {
  @Library('JenkinsSharedLib@master') _    
    
  stage("FirstStage") {
    sh "echo 'Hey hello'"
  }
  
  stage("SecondStage") {
    InitUtils {
        echo 'buuuuuuu'
    }    
  }
  
  stage("ThirdStage") {
    otherUtils.doStuff()  
  }

  stage("FourthStage") {
    copiedUtils.doStuff()  
  }
}

