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
           archiveArtifacts artifacts: 'build/libs/**/*.jar', fingerprint: true
            junit 'build/reports/**/*.xml'
        }
  }
