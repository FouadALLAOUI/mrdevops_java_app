@Library('shared-library') _

pipeline {
    agent any

    parameters{
        choice(name: 'action', choices: 'create\ndelete', description: 'Choose cteate/Destroy')
    } 

    stages {
        stage('Git Checkout') {
            when{ expression{ params.action == 'create' }}
            steps {
                gitCheckout(
                    branch: 'main',
                    url: 'https://github.com/FouadALLAOUI/mrdevops_java_app.git'
                )
            }
        }
        stage('Unit Test maven') {
            when{ expression{ params.action == 'create' }}
            steps {
                script{
                   mvnTest()
                }
            }
        }
        stage('Integration Test maven') {
            when{ expression{ params.action == 'create' }}
            steps {
                script{
                   mvnIntegrationTest()
                }
            }
        }
        //squ_8cea23e7ed22c2ad1a0fcff87134337760b14398
        stage('Static Code Analysis : Sonarqube') {
            when{ expression{ params.action == 'create' }}
            steps {
                script{
                   statiCodeAnalysis()
                }
            }
        }

    }
}
