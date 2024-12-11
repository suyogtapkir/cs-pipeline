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
        failure {
		    mail to: 'suyogtapkir1152@gmail.com',
		    Subject: "Failed pipeline: ${currentBuild.fullDisplayName}",
		    body: "ALARM, Please fix ${env.BUILD_URL}"
	    }
	    success {
		    mail to: 'suyogtapkir1152@gmail.com',
		    Subject: "Success pipeline: ${currentBuild.fullDisplayName}",
		    body: "Congratulations!,  Build is successful ${env.BUILD_URL}"
	    }
    }
}
