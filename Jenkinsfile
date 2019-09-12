node {
    stage('checkout') {
        checkout scm
    }

    stage ('npm install') {
        echo "node modules setup"
        bat "npm install"
        bat "npm audit fix --force"
        bat "npm install -g ionic cordova@8.1.2"
    }
    stage ('build') {
        echo "build started"
        
        bat  "cordova build andorid"
    }
}

