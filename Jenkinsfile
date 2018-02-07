@Library('JenkinsSharedLib@master') _  

libs = [:]
libPath = "/var/jenkins_home/xxxx/CopiedLib/vars/"

node('master') {
   stage('Init data') {
     sh 'ls'
     sh 'pwd'

     loadAllFiles(createFilePath(libPath))
   } 
}


node('TestNode') {
   

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
    libs['copiedUtils'].doStuff()  
  }
}

def loadAllFiles(rootPath) {
    for (subPath in rootPath.list()) {
        echo 'in Loop'
        echo subPath.getName()
	    echo 'in Loop xxxxx'
        if (!subPath.isDirectory()) {
           echo 'trying to load library'
 	       fileName = subPath.getName().replaceAll('.groovy', '')
          
           libs[fileName] = load "/var/jenkins_home/xxxx/CopiedLib/vars/${fileName}.groovy"

	    }
    }
}

// Helps if slave servers are in picture
def createFilePath(def path) {
    echo path
    if (env['NODE_NAME'].equals("master")) {
        File localPath = new File(path)
        return new hudson.FilePath(localPath);
    } else {
        return new hudson.FilePath(Jenkins.getInstance().getComputer(env['NODE_NAME']).getChannel(), path);
    }
}

