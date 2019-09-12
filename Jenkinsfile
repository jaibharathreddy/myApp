node {
    stage('checkout') {
        checkout scm
    }

    stage ('npm install') {
        echo "node modules setup"
        bat "npm install"
        bat "npm audit fix --force"
        bat "npm install -g cordova@8.1.2"
        bat "npm install -g cordova@5.2.3"
    }
    stage ('build') {
        echo "build started"
        
        bat  "cordova build andorid"
    }
}

