#!groovy


node {
  echo 'Entered into the node'
checkout scm
  stage('Maven') {
     withEnv(["PATH+MAVEN=${tool 'M3'}/bin"]) {
     sh "mvn clean verify"
     }
   }
        always {
            archive "target/**/*"
            junit 'target/surefire-reports/*.xml'
        }
}

