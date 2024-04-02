def unitTests() {
  stage('Unit Tests') {
    echo 'OK'
  }
}

def integrationTests() {
  stage('Integration Tests') {
    echo 'OK'
  }
}

def codeQuality() {
  stage('Code Quality') {
    echo 'OK'
  }
}

def sast() {
  stage('SAST') {
    echo 'OK'
  }
}

def sca() {
  stage('SCA') {
    echo 'OK'
  }
}

def secretDetection() {
  stage('SECRET Detection') {
    echo 'OK'
  }
}

def artifactProduce() {
  stage('Produce Artifact') {
    echo 'ok'
  }
}

def codeCheckout() {
  stage('CodeCheckout') {
    echo 'ok'
  }
}

def codeDeploy() {
  stage('Dev Deployment') {
      echo 'ok'
    }
  }


node('workstation') {

  codeCheckout()

  if(env.BRANCH_NAME == 'main') {
    codeQuality()
  }
  else if (env.TAG_NAME ==~ '.*') {
    sast()
    sca()
    secretDetection()
    artifactProduce()
    codeDeploy()
  }
  else if(env.BRANCH_NAME ==~ '.*') {
    unitTests()
    integrationTests()
    codeQuality()
  }
}

