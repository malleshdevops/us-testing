def stagename = ""
pipeline {
    agent any

    stages {
        stage('Hello') {
            steps {
                echo 'Hello World'
				script{
				 stagename = "Hello"
				}
            }
            post{
                aborted{
            emailext attachLog: true, body: 'devops15 ', compressLog: true, subject: ' stagename: ${stagename} jenkins options testing', to: 'malleshdevops2021@gmail.com'
            }
            }
        }
        stage('maven build'){
            steps{
                echo 'maven build status'
                sh 'sleep 60s'
            }
            post{
                aborted{
            emailext attachLog: true, body: 'devops15 ', compressLog: true, subject: 'jenkins options testing', to: 'malleshdevops2021@gmail.com'
            }
            }
        }
        stage('email notification'){
            steps{
                echo "email notification"
            }
            post{
                aborted{
            emailext attachLog: true, body: 'devops15 ', compressLog: true, subject: 'jenkins options testing', to: 'malleshdevops2021@gmail.com'
            }
            }
        }
    }
    post {
        fixed{
            emailext attachLog: true, body: 'devops15 ', compressLog: true, subject: 'jenkins options testing', to: 'malleshdevops2021@gmail.com'
        }
        aborted{
            emailext attachLog: true, body: 'devops15 ', compressLog: true, subject: 'jenkins options testing', to: 'malleshdevops2021@gmail.com'
        }
        success{
            emailext attachLog: true, body: 'devops15 ', compressLog: true, subject: 'jenkins options testing', to: 'malleshdevops2021@gmail.com'
        }
    }
}
