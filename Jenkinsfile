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
                echo 'excuting gradle...'
                withGradle() {
                    sh './gradlew -v'
                }
            }
        }
    }
}