@Library('SdlcLight@master') _  
libPath = "/var/jenkins_home/workspace/pipelines/JenkinsSharedLib/vars"

def libs = libraryLoader.loadLibraries([libPath])
libs.SDLC_NODE('TestNode') {
   
  libs.stage("FirstStage") {
    sh "echo 'Hey hello'"

    libs.each{
	    key, value -> print key;
	}
  }
  
  libs.stage("SecondStage") {
  	print libs['InitUtils']
    libs['InitUtils'] {
        echo 'buuuuuuu'
    }    
  }
  
  libs.stage("ThirdStage") {
    libs.otherUtils.doStuff()  
  }

  libs.stage("FourthStage") {
    //libs['copiedUtils'].doStuff()  
  }
}
