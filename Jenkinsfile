//@Library('jenkins_shared_lib') _

pipeline {
    agent any
    stages {
        stage('Git Checkout') {
            steps {
                script{
                    git branch: 'main', url: 'https://github.com/FouadALLAOUI/mrdevops_java_app.git'
                }
            }
        }
        //stage('Git Checkout') {
        //    steps {
        //        gitCheckout(
        //            branch: 'main',
        //            url: 'https://github.com/FouadALLAOUI/mrdevops_java_app.git'
        //        )
        //    }
        //}
        //stage('Unit Test maven') {
        //    steps {
        //        script{
        //           mvnTest()
        //        }
        //    }
        //}

    }
}
