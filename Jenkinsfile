node {
    stage('checkout') {
        checkout scm
    }

    stage ('npm install') {
        echo "node modules setup"
        bat "npm install"
        bat "npm audit fix --force"
    }
    stage ('platform adding') {
        echo "adding started" 
        bat  "ionic cordova platform remove android"   
        bat  "ionic cordova platform add android"
    }
    stage ('platform build') {
        echo "build started"
        bat  "ionic cordova build android"
    }
}

