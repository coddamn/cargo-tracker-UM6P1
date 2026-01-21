pipeline {
    agent any

    triggers {
        githubPush()   
    }

    stages {

        stage('Clone') {
            steps {
                git branch: 'develop', url: 'https://github.com/coddamn/cargo-tracker-UM6P1.git'
            }
        }

        stage('Build & Test') {
            steps {
                bat 'mvnw.cmd clean verify'
    }
}


    }
//
    post {
        success {
            echo 'Build et analyse terminés avec succès !'
        }
        failure {
            echo 'Échec du build ou des tests.'
        }
    }
}
