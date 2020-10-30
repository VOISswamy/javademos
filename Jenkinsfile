pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        sh 'mvn -f ssgsems/pom.xml -B -DskipTests clean package'
        archiveArtifacts(artifacts: '**/target/*.war ', fingerprint: true)
      }
    }

  }
}