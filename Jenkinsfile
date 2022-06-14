pipeline{
  agent {
    label 'testLinux'
  }
  stages{
    stage('Prepare Codebase'){
      steps {
        echo "This is Sample Java Project with mvn"
        mvn version
        sh 'java -version'
      }
    }
  }
}
