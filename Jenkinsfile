pipeline {
    agent any

    environment {
        MAVEN_HOME = tool 'Maven3' // Make sure Maven3 is configured in Jenkins
        PATH = "${MAVEN_HOME}/bin:${PATH}"
    }

    stages { 
        stage('Checkout') {
            steps {
                git branch: 'master', url: 'https://github.com/Vinayakumarw/sparkjava-war-example.git'
            }
        }

        stage('Build') {
            steps {
                sh 'mvn clean install'
            }
        }

        stage('Deploy') {
            steps {
                sh 'mvn deploy'
            }
        }
    }
}
   
