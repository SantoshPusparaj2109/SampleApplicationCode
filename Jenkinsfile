pipeline{
    agent any
    stages{
        stage("Git Checkout"){
            steps{
                script{
                    git branch: 'development', url: 'https://github.com/SantoshPusparaj2109/SampleApplicationCode.git'
                }
            }
        }
    }
}