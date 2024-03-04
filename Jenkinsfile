
pipeline {
    agent {label 'slave-1'}
    stages {
        stage('GIT Checkout') {
            steps{
                  git 'https://github.com/OpqTech/java-example1'
			}
        }

        stage('Build') {
            steps {
                    sh 'mvn clean install' 
            }
        }

        stage('Deploy') {
            steps {

	      // script {
                 //   def scannerHome = tool 'Sonar-qube1'
                   // withSonarQubeEnv('Sonar_qube') {
                        sh "mvn sonar:sonar""}
echo "clean"}
        }
		}}
}
