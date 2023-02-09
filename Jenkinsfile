node {
  stage('SCM') {
    checkout scm
  }
  stage('SonarScanner Analysis') {
    def scannerHome = tool 'SonarScanner';
    withSonarQubeEnv('SonarQube') {
      sh "${scannerHome}/bin/sonar-scanner"
    }
  }
}
