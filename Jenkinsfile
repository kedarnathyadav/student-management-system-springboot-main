pipeline {
    agent any
    stages {
	 stage('compile and clean') {
            steps {
		sh "mvn compile"
            }
        }
        stage('Deploy') {
            steps {
                sh "mvn dependency:copy-dependencies"
            }
	}
		stage('Execution') {
            steps {
                sh "java -jar target/student-management-system-springboot-main-0.0.1-SNAPSHOT.jar"
            }
	}

    }
}
