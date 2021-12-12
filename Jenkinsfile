def d = [
  'terraform.version':'1.0.0',
  'tfsec.version':'v0.57.1',
  'tflint.version':'v0.32.0'
]

def props = [:]

podTemplate {
  node('DANISH_MACHINE') {
    checkout scm
    props = readProperties(defaults: d, file: 'version.properties')
  }
}

pipeline {
  agent {
    label 'DANISH_MACHINE'   
  }
  stages
  {
  stage
    {
    echo '${props["terraform.version"]}'
    }
  }
}
