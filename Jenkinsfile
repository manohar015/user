@Library('robot-shared-library@main') _

pipeline {
    agent any
    stages {
        stage('Downloading the dependencies') {
            steps {

                sh "npm install"
            }
        }
        stage('Lint Checks') {
            steps {
                script {
                    sample.info("Welcome", "Stockexchange.com")
                }
                sh "echo installing jslint"
                sh "npm i jslint"
                sh "node_modules/jslint/bin/jslint.js server.js"
            }
        }
    }

}