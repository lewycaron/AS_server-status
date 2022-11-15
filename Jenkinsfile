/* groovylint-disable-next-line CompileStatic */
pipeline {
    agent any

    tools {
        gradle '7.6-rc-3'
    }

    stages {
        stage('run frontend'){
            steps {
                echo 'excuting yarn...'
                nodejs('Node-19') {
                    sh 'yarn install'
                }
            }
        }
        stage('run backend') {
            steps {
                echo 'executing gradle...'
                sh 'gradle --version'
            }
        }
        stage('Aws') {
            steps {
                sh './aws/install'
                sh 'aws --version'
            }
        }
    }
}
