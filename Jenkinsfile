node {
    stage('checkout') {
        checkout scm
    }

    stage ('npm install') {
        echo "node modules setup"
        sh "npm install"
        sh "npm audit fix --force"
    }
    stage ('build') {
        echo "build started"
        sh  "ionic cordova platform add android"
    }
}

