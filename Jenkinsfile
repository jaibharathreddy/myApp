node {
    stage('checkout') {
        checkout scm
    }

    stage ('npm install') {
        echo "node modules setup"
        bat "npm install"
        bat "cordova -v"
        bat "ionic -v"
        bat "npm audit fix --force"
    }
    stage ('platform adding') {
        echo "adding started" 
        bat  "cordova platform remove android"   
        bat  "icordova platform add android"
    }
    stage ('platform build') {
        echo "build started"
        bat  "cordova build android"
    }
}

