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
  }
}
