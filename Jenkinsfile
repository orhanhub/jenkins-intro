//Scripted pipeline
node {
    try {
        stage('Checkout') {
            checkout scm
        }
        stage('Environment') {
            sh 'git --version'
            sh 'docker -v'
        }
    stage ('Build Docker'){
        sh 'docker build -t yararo/express-server .'
        sh 'docker run -p 49160:8080 -d yararo/express-server'
    }
    }
    catch (err) {
        throw err
    }
}