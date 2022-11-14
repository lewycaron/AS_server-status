pipeline {
    agent any
    stages {
        stage("run frontend") {
            steps {
                echo 'excuting yarn...'
                nodejs('Node-10.17') {
                    bat 'yarn install'
                }
            }
        }
        stage("run backend") {
            steps {
                echo 'excuting gradle...'
                withGradle() {
                    bat './gradlew -v'
                }
            }
        }
    }
}