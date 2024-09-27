pipeline {
    agent any
    tools {
        // Install the Maven version configured as "maven-398" and add it to the path.
        maven "maven-398"
    }
    stages {
        stage('Build') {
            steps {
                // Get some code from a Git repository
		git branch: 'main', url: 'http://localhost:3000/dasher-org/jenkins-hello-world.git'
                sh "mvn clean package -DskipTests=true"
		// Add other build steps here
            }
}
	stage('Unit Test'){
	    steps {

			sh "mvn test"
		   }
    }
}

}
