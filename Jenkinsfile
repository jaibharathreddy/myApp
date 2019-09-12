node {
    stage('checkout') {
        checkout scm
    }

    stage ('npm install') {
        echo "node modules setup"
        bat "npm install"
        bat "npm audit fix --force"
    }
    stage ('build') {
        echo "build started"
        bat "ionic cordova build andorid"
    }
}

