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

                // Make the Maven Wrapper script executable
                sh 'chmod +x mvnw'
                
                // Use the Maven Wrapper to build and test the project
                sh './mvnw clean install'
            }
        }


    }
}
