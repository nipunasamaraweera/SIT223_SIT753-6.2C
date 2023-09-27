pipeline{
    agent any
    stages{
        stage("Build"){
            steps{
                echo "Building ..."
            }
            post{
                always{
                    mail to: "thathsarasamaraweera16@gmail.com",
                    subject: "Build Status Email",
                    body: "Build log attached!"
                    attachlog : true
                }
            }
        }
        stage("Test"){
            steps{
                echo "Testing ..."
                echo "static code analysis by SonarQube"
                echo "Automataion testing by maven"
                echo "Running unit testing by Junit testing"
                echo "Running Security testing by OWASP ZAP"
            }
        }
        stage("Deploy"){
            steps{
                echo "Deploying ..."
                echo " Deploying into AWS E2C"
            }
        }
        stage("Complete"){
            steps{
                echo "Completed."
            }
        }
    }
}
