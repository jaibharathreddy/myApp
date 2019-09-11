node {
    stage("Checkout") {
        checkout scm
    }

    stage("Prepare") {
        echo "add dependancies"
        sh 'npm install'
        sh "npm audit fix --force"
        sh "cordova platform rm android"
        sh "cordova platform add android@8.0.0"
        sh "cordova prepare android"
        sh 'cordova build android'
    }

     stage("build platform") {
        echo "build platforms"
        sh 'cordova build android'
    }