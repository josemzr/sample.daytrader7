pipeline {
    agent any
    stages {
        stage('Construccion con Maven') {
            steps {
                sh '''
		   whoami
                   echo "BUILD NUMBER: ${BUILD_NUMBER}"
		   docker run --rm --name maven-build -v "$(pwd)":/usr/src/mymaven -w /usr/src/mymaven maven:3.3-jdk-8 mvn clean install
                   '''
             }
        }
    }
}
