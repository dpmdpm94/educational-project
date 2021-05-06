pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo 'Start building'
		sh './gradlew build'
                archiveArtifacts artifacts: 'build/libs/*.jar', fingerprint: true
		echo 'Building is done'
            }
        }
        stage('Test') {
            steps {
                echo 'Testing..'
            }
        }
        stage('Deploy') {
	    environments {
             myVar = "oki doki"
 	    }
            steps {
                echo "Deploying.... the ${env.BUILD_ID} on ${env.JENKINS_URL} build is:  ${myVar}"
            }
        }
    }
}
