#!groovy

stage('Initialization') {
  checkout scm
} 

node {
stage('Maven') {
withEnv(["PATH+MAVEN=${tool 'M3'}/bin"]) {
    sh "mvn clean verify"
}
}
}
