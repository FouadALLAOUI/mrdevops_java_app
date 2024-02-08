@Library('shared-library') _

pipeline {
    agent any

    parameters{
        choice(name: 'action', choices: 'create\ndelete', description: 'Choose cteate/Destroy')
    } 

    stages {
        stage('Git Checkout') {
            when{ expression{ param.action == 'create' }}
            steps {
                gitCheckout(
                    branch: 'main',
                    url: 'https://github.com/FouadALLAOUI/mrdevops_java_app.git'
                )
            }
        }
        stage('Unit Test maven') {
            when{ expression{ param.action == 'create' }}
            steps {
                script{
                   mvnTest()
                }
            }
        }
        stage('Integration Test maven') {
            when{ expression{ param.action == 'create' }}
            steps {
                script{
                   mvnIntegrationTest()
                }
            }
        }

    }
}
