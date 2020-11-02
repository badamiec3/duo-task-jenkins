pipeline {
  agent any
  stages {
      stage('Get Repo') {
        steps {
            sh 'chmod a+x ./scripts/get-repo.sh'
            sh './scripts/get-repo.sh'
        }
      }
      stage('docker') {
        steps {
            sh 'chmod a+x ./scripts/docker.sh'
            sh './scripts/docker.sh'
        }
      }
      stage('push to nexus') {
        steps {
            sh 'chmod a+x ./scripts/nexus.sh'
            sh './scripts/nexus.sh'
        }
      }
   }
}
