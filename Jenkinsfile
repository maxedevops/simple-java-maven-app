piepline {
  agent any

  tools {
    maven 'Maven 3.9.9'
    jdk 'OpenJDK 21'
  }
  stages{
    stage('Build') {
      steps {
        sh 'mvn clean compile'
      }
    }
    stage('Test'){
      steps{
        sh 'mvn test'
      }
    }
    stage('Package'){
      steps {
        sh 'mvn package'
      }
    }
  }
  post {
    always {
      junit '**/target/surefire-reports/*.xml'
    }
  }
}
      
