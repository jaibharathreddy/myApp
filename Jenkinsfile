pipeline {
   stages {
      stage('NPM Setup') {
      steps {
         sh 'npm install'
      }
   }

   stage('Android Build') {
   steps {
      sh 'ionic cordova build android'
   }
  }
 }
}


