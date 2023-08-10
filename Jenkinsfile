pipeline {
    agent any
    
    stages {
        stage('Build') {
            steps {
                // Check out the code from Git repository
                git branch: 'master', url: 'https://github.com/Nav9n/petadopt.git'

                sh "./mvnw clean compile"
                echo 'Building the project with maven compile'
            }
        }

        stage('Test'){
            steps{

                sh "./mvnw clean test"
                echo 'Testing the project with maven test'
            }
        }

        
    }
}
