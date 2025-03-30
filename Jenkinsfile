pipeline {
    agent any

	environment {
        NODE_VERSION = '22'
    }

    stages {
	stage('Prepare') {
            steps {
		echo 'Preparing..'
                script {
                    echo "Installing Node.js v${NODE_VERSION}"
                    sh 'node -v || curl -fsSL https://deb.nodesource.com/setup_22.x | sudo -E bash - && sudo apt-get install -y nodejs'
                }
            }
        }
        stage('Build') {
            steps {
                echo 'Building..'
		script {
                    echo 'Checking npm version...'
                    sh 'npm -v'
                }
            }
        }
        stage('Test') {
            steps {
                echo 'Testing..'
		script {
                    echo 'Displaying JENKINS_URL...'
                    sh 'echo $JENKINS_URL'
                }
            }
        }
    }
}
