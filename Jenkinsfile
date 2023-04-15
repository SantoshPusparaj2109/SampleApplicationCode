@Library ("jenkins_shared_library") _
pipeline{
    agent any
    stages{
        stage("Git Checkout"){
            steps{
                gitCheckout(
                    branch: "development",
                    url: "https://github.com/SantoshPusparaj2109/SampleApplicationCode.git"
                )
            }
        }
        stage("Maven Test"){
            steps{
                script
                {
                    mvnTest()
                    }
            }
        }
    }
}