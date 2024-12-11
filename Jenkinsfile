pipeline{
    agent {
        node {
            label 'maven_build_server'
        }
    }
    stages{
        stage("Intialize the project"){
            steps{
                echo "this step is to initialize the project  j"     
            }
        }
        stage("Build"){
            steps{
                echo "this step is to build the project"
            }
        }
        stage("Test"){
            steps{
                echo "this step is to test the project"
            }
        }
        stage("deploy"){
            steps{
                echo "this step is to deploy the project147296"
            }
        }

    }
    post {
        always{
            emailext body: 'A Test EMail', recipientProviders: [[$class: 'DevelopersRecipientProvider'], [$class: 'RequesterRecipientProvider']], subject: 'Test'
        }
    }
}
