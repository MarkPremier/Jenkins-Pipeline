pipeline{
    agent any
    environment{
        DIRECTORY_PATH= "/codefolder/final"
        TESTING_ENVIRONMENT= "Jenkins Environment"
        PRODUCTION_ENVIRONMENT= "MarkP"
    }
    stages{
        stage("Build"){
            steps{
                echo "fetch the source code from the directory path specified by the environment variable"
                echo "$DIRECTORY_PATH"
                echo "compile the code and generate any necessary artifacts"
            }
            post{
                success{
                    mail to:"markpremier@gmail.com",
                    subject:"Build Status Email",
                    body:"Build was successful!"
                }
            }
        }
        stage("Test"){
            steps{
                echo "Unit Tests"
                echo "Integration Tests"
            }
        }
        stage("Code Quality Check"){
            steps{
                echo "Check the quality of the code"
            }
        }
        stage("Deploy"){
            steps{
                echo "deploy the application to a testing environment specified by the environment variable"
                echo "$TESTING_ENVIRONMENT"
            }
        }
        stage("Approval"){
            steps{
                bat 'ping -n 10 localhost'
            }
        }
        stage("Deployment to Production"){
            steps{
                echo "Deploy to $PRODUCTION_ENVIRONMENT production environment"
            }
        }
    }
}
