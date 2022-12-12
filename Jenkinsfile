
pipeline{
    agent any

    stages{

        stage('login server'){

            steps{
            sshagent(credentials:['Jenkins-server']){

                sh 'ssh  -o StrictHostKeyChecking=no  root@172.31.13.73 uptime "whoami"'

                sh 'rsync -avh /var/lib/jenkins/workspace/job-1/Dockerfile root@172.31.13.73:/opt/'

            }

                echo "success lgoin"

            }
        }
    }
}
