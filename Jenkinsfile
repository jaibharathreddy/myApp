node {
    stage('checkout') {
        checkout scm
    }

    stage ('npm install') {
        echo "node modules setup"
        sh "npm install"
        sh "cordova -v"
        sh "ionic -v"
        bat "npm audit fix --force"
    }
    stage ('platform adding') {
        echo "adding started" 
        sh  "cordova platform remove android"   
        sh "cordova platform add android"
    }
    stage ('platform build') {
        echo "build started"
        sh  "cordova build android"
    }
}

