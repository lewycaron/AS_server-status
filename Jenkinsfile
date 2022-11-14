pipeline {
    agent any

    stages {
        stage("run frontend") {
            steps {
                echo 'excuting yarn...'
                nodejs('Node-19') {
                    sh 'yarn install'
                }
            }
        }
        stage("run backend") {
            steps {
                echo 'executing gradle...'
                withGradle() {
                    sh 'gradle --version'
                }
            }
        }
    }
}