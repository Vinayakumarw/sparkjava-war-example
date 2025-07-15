pipeline {
    agent any

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
   
