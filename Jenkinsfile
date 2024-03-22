pipeline {
  agent any
  stages {
    stage('scan') {
      steps {
        sh "docker run -v ${WORKSPACE}:/src --workdir /src semgrep/semgrep:latest semgrep --config p/ci --config p/security-audit --config p/secrets"
      }
    }
  }
}
