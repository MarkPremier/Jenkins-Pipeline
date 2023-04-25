pipeline{
    agent any
    stages{
        stage("Build"){
            steps{
                echo "Building using webpack"
                echo "Code has been compiled and packaged"
            }
        }
        stage("Unit and Integration Tests"){
            steps{
                echo "Unit testing done by Selenium"
                echo "Testing if code is functioning as expected"
                echo "Integration testing done by Citrus"
                echo "Testing if components of application are working as expected"
            }
             post{
                success{
                    emailext attachLog: true, to:"markpremier@gmail.com",
                    subject:"Test Status Email",
                    body:"Test was successful!"
                }
                failure{
                    emailext attachLog: true, to:"markpremier@gmail.com",
                    subject:"Test Status Email",
                    body:"Testing has failed!"
                }
            }
        }
        stage("Code Analysis"){
            steps{
                echo "Code analysis completed using SonarQube"
                echo "Code meets industry standards"
            }
        }
        stage("Security Scan"){
            steps{
                echo "Security scan using Snyk"
                echo "Testing for any vulnerabilities"
            }
             post{
                success{
                    emailext attachLog: true, to:"markpremier@gmail.com",
                    subject:"Security Scan Status Email",
                    body:"Security Scan was successful, no vulnerabilities found"
                }
                failure{
                    emailext attachLog: true, to:"markpremier@gmail.com",
                    subject:"Security Scan Status Email",
                    body:"Build has failed, there are vulnerabilities"
                }
            }
        }
        stage("Deploy to Staging -"){
            steps{
                echo "Application deployed to Staging server on AWS EC2"
            }
        }
        stage("Integration Tests on Staging"){
            steps{
                echo "Integration testing done by Citrus"
                echo "Testing if components of application are working as expected"
            }
             post{
                success{
                    emailext attachLog: true, to:"markpremier@gmail.com",
                    subject:"Test Status Email",
                    body:"Test was successful!"
                }
                failure{
                    emailext attachLog: true, to:"markpremier@gmail.com",
                    subject:"Test Status Email",
                    body:"Testing has failed!"
                }
            }
        }
        stage("Deploy to Production"){
            steps{
                echo "Application deployed to production server on AWS EC2"
            }
        }
    }
}
