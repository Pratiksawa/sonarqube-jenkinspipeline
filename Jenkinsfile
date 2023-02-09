node {
  stage('SCM') {
    checkout scm
  }
  stage('SonarScanner Analysis') {
    def scannerHome = tool 'SonarScanner';
    withSonarQubeEnv() {
      sh "${scannerHome}/bin/sonar-scanner"
    }
  }
}
