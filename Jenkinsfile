

def props = [:]
def age= "AGE=27"
//podTemplate {
  node('DANISH_MACHINE'){
    checkout scm
	
	 prependToFile(file: 'version.properties', content: age)
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
	 echo "printing age"
		 echo "${props["AGE"]}"
	 
    }
	}
	}
  
}
}
