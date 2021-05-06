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
	    environment {
             myVar = "oki doki"
 	    }
            steps {
             echo 'this is another branch to test
	    }
        }
    }
}
