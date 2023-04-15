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
    }
}