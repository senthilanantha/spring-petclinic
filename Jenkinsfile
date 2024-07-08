pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        sh './mvnw clean compile'
      }
    }

    stage('Static Analysis') {
      steps {
        sh '''mvnw sonar:sonar \\
  -Dsonar.projectKey=Petclinic \\
  -Dsonar.projectName=\'Petclinic\' \\
  -Dsonar.host.url=http://3.110.138.237:9000 \\
  -Dsonar.token=sqp_63e8540c184e7b6d7f5ad84f6f3832c83f8cb4a9'''
      }
    }

  }
}