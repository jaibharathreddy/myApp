node {
    stage('checkout') {
        checkout scm
    }

    stage ('npm install') {
        echo "node modules setup"
        sh "npm install"
        sh "npm audit fix --force"
    }
    stage ('platform adding') {
        echo "adding started" 
        sh  "ionic cordova platform remove android"
        sh  "ionic cordova resources"
        sh  "ionic cordova platform add android@8.0.0"
    }
    stage ('platform build') {
        echo "build started"
        sh  "ionic cordova build android"
    }
}

