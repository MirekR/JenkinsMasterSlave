@Library('SdlcLight@master') _  
libPath = "/var/jenkins_home/workspace/pipelines/JenkinsSharedLib/vars"

SDLC_NODE('TestNode', [libPath]) {libs ->
   
  stage("FirstStage") {
    sh "echo 'Hey hello'"

    libs.each {
	    key, value -> print key;
	}
  }
  
  stage("SecondStage") {
  	print libs['InitUtils']
    InitUtils {
        echo 'buuuuuuu'
    }    
  }
  
  stage("ThirdStage") {
    otherUtils.doStuff()  
  }

  stage("FourthStage") {
    //libs['copiedUtils'].doStuff()  
  }
}
