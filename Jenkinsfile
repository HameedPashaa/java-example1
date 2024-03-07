pipeline {
    agent any
    stages {
        stage('GIT Checkout') {
            steps {
               echo "chslcj"
            
        }}

        stage('Build') {
            steps {
                // Use Maven tool to run Maven commands
                sh 'mvn clean install'
            }
        }
stage('SonarQube Analysis') {
            steps {
                // Execute SonarQube scanner
                withSonarQubeEnv('sonarqube') {
                    sh 'mvn sonar:sonar'
                }
            }
        
        stage('Deploy') {
            steps {
             
                {
                  echo  "sh mvn sonar:sonar"
                }
            }
        }
    }
}
