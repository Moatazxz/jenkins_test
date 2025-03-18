pipeline {
    agent any

    stages {
       

        stage('Run Script') {
            steps {
                sh 'chmod +x test.sh'  // Make script executable
                sh './test.sh'  // Run the script
            }
        }

           stage('Connect to EC2 and Run Command') {
            steps {
                sshagent(credentials: [PK_EC2]) {
                    sh """
                    ssh -o StrictHostKeyChecking=no ec2-user@18.232.54.212 'uname -a'
                    """
                }
            }
        }

        
    }


    
}
