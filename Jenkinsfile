node {
    stage("Checkout") {
        checkout scm
    }


    stage("Prepare") {
        echo "add dependancies"
        sh "npm install"
        sh "npm audit fix --force"
    }

    
}