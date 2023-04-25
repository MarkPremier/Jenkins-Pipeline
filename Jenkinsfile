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
                    mail to:"markpremier@gmail.com",
                    subject:"Build Status Email",
                    body:"Build was successful!"
                }
                failure{
                    mail to:"markpremier@gmail.com",
                    subject:"Build Status Email",
                    body:"Build has failed"
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
            post{
                success{
                    mail to:"markpremier@gmail.com",
                    subject:"Build Status Email",
                    body:"Build was successful!${BUILD_LOG, maxLines=9999, escapeHtml=false}"
                }
                failure{
                    mail to:"markpremier@gmail.com",
                    subject:"Build Status Email",
                    body:"Build has failed ${BUILD_LOG, maxLines=9999, escapeHtml=false}"
                }
            }
        }
        stage("Staging Test"){
            steps{
                echo "Test using"
            }
            post{
                success{
                    mail to:"markpremier@gmail.com",
                    subject:"Build Status Email",
                    body:"Build was successful! ${BUILD_LOG, maxLines=9999, escapeHtml=false}"
                }
                failure{
                    mail to:"markpremier@gmail.com",
                    subject:"Build Status Email",
                    body:"Build has failed ${BUILD_LOG, maxLines=9999, escapeHtml=false}"
                }
            }
        }
        stage("Deploy"){
            steps{
                echo "Deploying..."
            }
        }
    }
}
