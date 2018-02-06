node('TestNode') {
  @Library('JenkinsSharedLib@master') _    
    
  stage("FirstStage") {
    sh "echo 'Hey hello'"
    
    InitUtils {
        echo 'buuuuuuu'
    }    
  }
  
  stage("SecondStage") {
    InitUtils {
        echo 'buuuuuuu'
    }    
  }
  
  stage("ThirdStage") {
    otherUtils.doStuff()  
  }
}

