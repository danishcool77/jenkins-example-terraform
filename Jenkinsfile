def d = [
  'terraform.version':'1.0.0',
  'tfsec.version':'v0.57.1',
  'tflint.version':'v0.32.0'
]

def props = [:]

podTemplate {
  node {
    checkout scm
	prependToFile(file: 'version.properties', content: 'NAME:DANISH')
    
	
  }
}

pipeline {
  agent any
  stages
  {
  stage('prop-file-reading')
    {
	steps
	{
		props = readProperties(defaults: d, file: 'version.properties')
    echo "${props["terraform.version"]}"
		 echo "${props["DANISH"]}"
    }
	}
  }
}
