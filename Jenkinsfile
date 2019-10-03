pipeline {
  agent { label 'linux'}
  tools {
    maven 'M3'
  }
  stages {
   stage("checkout"){
    steps {
      git "https://github.com/cfdistortion/myProject.git"
    }
   }
   stage('build') {
     steps {
       sh 'mvn clean compile'
     }
   }
 
   }
   stage('Package') {
     steps {
       sh 'mvn package'
     }
   }
  }
}
