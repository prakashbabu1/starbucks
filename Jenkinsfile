#!groovy​

node {
    def mvnHome = tool 'M3'

    stage('Checkout') {
        checkout scm
    }

    stage('Build') {
        sh "${mvnHome}/bin/mvn -B package -DskipTests=true"
    }

    stage('Unit Tests') {
        sh "${mvnHome}/bin/mvn -B test"
    }
}