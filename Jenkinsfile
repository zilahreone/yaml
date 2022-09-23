pipeline {
 
  agent {
    kubernetes {
      yamlFile 'build-agent.yaml'
      defaultContainer 'alpine'
      idleMinutes 1
    }
  }
  stages {
    stage('Sample Stage') {
      parallel {
        stage('this runs in a pod') {
          steps {
            container('alpine') {
              sh 'uptime'
            }
          }
        }
      }
    }
    }
}
