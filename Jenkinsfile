pipeline{
  agent {
    label 'testLinux'
  }
  stages{
    stage('Prepare Codebase'){
      echo "This is Sample Java Project with mvn"
      mvn --version
      sh 'java -version'
    }
}
