node {
    stage('checkout') {
        checkout scm
    }

    stage ('npm install') {
        echo "node modules setup"
        bat "npm install"
        bat "npm audit fix --force"
        bat "npm install ionic cordova"
    }
    stage ('build') {
        echo "build started"
        bat  "cordova build andorid"
    }
}

