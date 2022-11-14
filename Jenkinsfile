pipeline {
    agent any
    stages {
        stage("run frontend") {
            steps {
                echo 'excuting yarn...'
                nodeJs('Node-10.17') {
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