pipeline {
    agent any

    stages {
       

        stage('Run Script') {
            steps {
                sh 'chmod +x test.sh'  // Make script executable
                sh './test.sh'  // Run the script
            }
        }
    }
}
