@Library('SdlcLight@master') _  
libPath = "/var/jenkins_home/workspace/pipelines/JenkinsSharedLib/vars"
// libPath = "/var/jenkins_home/workflow-libs/JenkinsSharedLib/vars"

SDLC_NODE('TestNode', [libPath]) { libs ->
   
  stage("FirstStage") {
    sh "echo 'Hey hello'"

    libs.each{
	    key, value -> print key;
	}
  }
  
  stage("SecondStage") {
  	print libs['InitUtils']
    // libs['InitUtils'] {
    //     echo 'buuuuuuu'
    // }    
  }
  
  stage("ThirdStage") {
    libs['otherUtils'].doStuff()  
  }

  stage("FourthStage") {
    //libs['copiedUtils'].doStuff()  
  }
}
