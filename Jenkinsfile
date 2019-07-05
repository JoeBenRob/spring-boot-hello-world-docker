pipeline{
        agent any
        stages{
                stage('---clean---'){
                        steps{
                                sh "mvn clean"
                        }
                }
                stage('--test--'){
                        steps{
                                sh "mvn test"
                        }
                }
                stage('--package--'){
                        steps{
                                sh "mvn package"
                        }
                }
		stage('--verify--'){
                        steps{
                                sh "mvn verify"
                        }
                }
		stage('--deploy--'){
                        steps{
                                sh "cd /"

				sh "sudo scp /var/lib/jenkins/workspace/${JOB_NAME}/target/hello-world-0.0.1-SNAPSHOT.jar  ssh joe@51.145.101.218:~/
                        }
                }
        }
}
