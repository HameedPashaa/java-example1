pipeline {
    agent any

    tools {
        // Define the Maven tool using the name configured in Jenkins
        maven 'MavenInstallation'
    }

    stages {
        stage('GIT Checkout') {
            steps {
                git 'https://github.com/OpqTech/java-example1'
            }
        }

        stage('Build') {
            steps {
                // Use Maven tool to run Maven commands
                sh 'mvn clean install'
            }
        }

        stage('Deploy') {
            steps {
                // Use Maven tool to run SonarQube analysis
               // withMaven(maven: 'MavenInstallation') 
                {
                    sh 'mvn sonar:sonar'
                }
            }
        }
    }
}
