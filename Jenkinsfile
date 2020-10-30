pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        sh 'mvn -f javademos-master/ssgsems/pom.xml -B -DskipTests clean package'
        archiveArtifacts(artifacts: '**/target/*.war ', fingerprint: true)
        sh '''mkdir /home/Swamy/buildoutput/${BUILD_NUMBER}
cp /var/lib/jenkins/workspace/javademos_master/javademos-master/ssgsems/target/ssgsems-0.0.2-SNAPSHOT.war /home/Swamy/buildoutput/${BUILD_NUMBER}'''
      }
    }

  }
}