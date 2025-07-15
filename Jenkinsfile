pipeline {
    agent any

    tools {
        // Install the Maven version configured as "M3" and add it to the path.
        maven "maven 3.9.10"
    }

    stages {
        stage('Github') {
            steps {
                // Get some code from a GitHub repository
                git branch: 'master', url: 'https://github.com/prasannakumarchowdary/Shopping-site-Project.git'
            }
        }
        
        stage('Build') {
            steps {
                // Run Maven on a Unix agent.
                sh "mvn -Dmaven.test.failure.ignore=true clean package"
            }
        }
    }
} 
