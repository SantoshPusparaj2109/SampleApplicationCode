@Library ("jenkins_shared_library") _
pipeline{
    agent any
    parameters{
        choice(name: 'action', choices: 'create\ndelete', description: 'Choose the action')
    }
    stages{
        
        stage("Git Checkout"){
            when { expression { param.action == "create" } }
            steps{
                gitCheckout(
                    branch: "development",
                    url: "https://github.com/SantoshPusparaj2109/SampleApplicationCode.git"
                )
            }
        }
        stage("Maven Test"){
            when { expression { param.action == "create" } }
            steps{
                script
                {
                    mvnTest()
                    }
            }
        }
        stage("Maven Integration Test"){
            when { expression { param.action == "create" } }
            steps{
                script
                {
                    mvnIntegrationTest()
                    }
            }
        }
        stage("Static Code Analysis: SonarQube"){
            when { expression { param.action == "create" } }
            steps{
                script
                {
                    staticCodeAnalysis()
                    }
            }
        }
    }
}