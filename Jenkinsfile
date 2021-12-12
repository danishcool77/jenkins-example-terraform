def d = [
  'city':'JAIPUR',
	
 ]

def props = [:]
def user= "'NAME'=DANISH'"
//podTemplate {
  node('DANISH_MACHINE'){
    checkout scm
	
	 prependToFile(file: 'version.properties', content: user)
	 props = readProperties( defaults:d, file: 'version.properties')
    
	
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
    }
	}
	}
  
}
}
