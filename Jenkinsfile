#!groovy


node {
  echo 'Entered into the node'
checkout scm
  stage('Maven') {
     withEnv(["PATH+MAVEN=${tool 'M3'}/bin"]) {
     sh "mvn clean verify"
     }
   }
  stage('TestPOC') {
   post {
  always {
    junit "path/to/xml"
     }
   }
  }
}

