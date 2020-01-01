pipeline {
    agent any
    stages {
        stage('Construccion con Maven') {
            steps {
                sh '''
                   echo "BUILD NUMBER: ${BUILD_NUMBER}"
		   docker run --rm --name my-maven-project -v "$(pwd)":/usr/src/mymaven -w /usr/src/mymaven maven:3.3-jdk-8 mvn clean install
                   '''
             }
        }
    }
}
