pipeline{

    agent any

    stages{

        stage('Git Chweckout'){

            steps{

                script{
                    // git branch: 'main', url: 'https://github.com/vikash-kumar01/mrdevops_java_app.git'
                    gitCheckout{
                        branch: "main",
                        url: "https://github.com/FouadALLAOUI/mrdevops_java_app.git"
                    }
                }
            }
        }
    }
}