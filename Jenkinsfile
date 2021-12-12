def d = [
  'terraform.version':'1.0.0',
  'tfsec.version':'v0.57.1',
  'tflint.version':'v0.32.0',
	'NAME':'SOHAIL'
]

def props = [:]
def user= 'NAME':'DANISH'
//podTemplate {
  node('DANISH_MACHINE'){
    checkout scm
	  prependToFile(file: 'version.properties', content: user)
	 props = readProperties(defaults: d, file: 'version.properties')
    
	
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
	{ 		//echo "${props["terraform.version"]}"
		 echo "${props["NAME"]}"
    }
	}
	}
  
}
}
