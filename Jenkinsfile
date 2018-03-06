#!groovy


node {
  try {
           echo 'Entered into the node'
           checkout scm
           stage('Maven') {
                 withEnv(["PATH+MAVEN=${tool 'M3'}/bin"]) {
                 sh "mvn clean verify"
           }
     }
  }finally {
            junit 'target/surefire-reports/*.xml'
        }
  }
