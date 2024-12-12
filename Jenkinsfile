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
        stage("Accept RFC number"){
            steps{
                script{
                    env.RFC=input message: 'Please enter RFC number', ok: 'Proceed:', parameters: [string(defaultValue: 'NA', description: 'RFC will be used to deploy in PROD', name: 'RFC Number')]
                    echo "RFC number is: ${RFC}"
                }
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
        failure {
		    emailext to: 'suyogtapkir1152@gmail.com',
		    subject: "Failed pipeline: ${currentBuild.fullDisplayName}",
		    body: "ALARM, Please fix ${env.BUILD_URL}"
	    }
	    success {
		    mail to: 'suyogtapkir1152@gmail.com',
		    subject: "Success pipeline: ${currentBuild.fullDisplayName}",
		    body: "Congratulations!,  Build is successful ${env.BUILD_URL}"
	    }
    }
}
