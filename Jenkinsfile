pipeline {
    agent any
    stages{
        stage('Init'){
            steps {
                echo 'Testing...'
            }
        }

        stage('Build'){
            steps {
                sh 'mvn clean package'
            }
            post {
                sucess {
                    echo 'Now Archiving'
                    archiveArtifacts artifacts: '**/target/*war'
                }
            }
        }

        stage('Deploy'){
            steps {
                echo 'Code deployed.'
            }
        }
    }
}
