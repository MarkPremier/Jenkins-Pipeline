pipeline{
    agent any
    stages{
        stage("Build"){
            steps{
                echo "Build using webpack!"
                echo "Code has been compiled and packaged!"
            }
        }
        stage("Unit Test"){
            steps{
                echo "Test using"
            }
             post{
                success{
                    emailext attachLog: true, to:"markpremier@gmail.com",
                    subject:"Build Status Email",
                    body:"Build was successful!"
                }
            }
        }
        stage("Analysis"){
            steps{
                echo "Analysis using"
            }
        }
        stage("Scan"){
            steps{
                echo "Security scan using"
            }
        }
        stage("Staging Test"){
            steps{
                echo "Test using"
            }
        }
        stage("Deploy"){
            steps{
                echo "Deploying..."
            }
        }
    }
}
