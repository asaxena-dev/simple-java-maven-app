pipeline{
  agent {
    label 'testLinux'
  }
  stages{
    stage('Prepare Codebase'){
      steps {
        echo "This is Sample Java Project with mvn"
        sh 'mvn --version'
        sh 'java -version'
      }
    }
    stage('Build'){
      steps{
        sh 'mvn -B -DskipTests clean package'
      }
    }
    stage('test'){
      steps {
        sh 'mvn test'
      }
    }
    stage('Publish Reports'){
      steps{
        junit 'target/surefire-reports/*.xml'
      }
    }
    stage('Delivery'){
      steps{
        sh './jenkins/scripts/deliver.sh'
      }
    }
  }
}
