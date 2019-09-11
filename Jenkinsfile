node {
    stage("Checkout") {
        checkout scm
    }


    stage("Prepare") {
        echo "add dependancies"
        sh 'npm install'
        sh "npm audit fix --force"
        sh "ionic cordova platform rm android"
        echo "removed platform"
        sh "ionic cordova platform add android"
        echo "added platform"
    }

     stage("build platform") {
        echo "build platforms"
        sh 'cordova build android'
    }
}