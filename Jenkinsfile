

def props = [:]

//podTemplate {
  node('DANISH_MACHINE'){
    checkout scm
		prependToFile(content: 'ADD=TEST', file: 'version.properties')
	
		 props = readProperties(file: 'version.properties')
    
	
  }
//}

pipeline {
	agent {
	
	label 'DANISH_MACHINE'
	}
  stages
  {
  stage('prop-file-reading')
    {

	steps
	{
	script
	{ 	echo "${props}"
		 echo "printing name"
		 echo "${props["NAME"]}"
	  echo "printing city"
		 echo "${props["CITY"]}"
	 echo "printing add"
		 echo "${props["ADD"]}"
	 
    }
	}
	}
  
}
}
