pipeline {
    agent {
        label 'node1'
    } 
    tools {
        maven 'maven3.8.4'
    }
    stages {
        stage('Build') {
            steps {
                sh 'mvn package'
            }
        }
        stage('Approval') {
            input {
                message 'do you want to deploy ?'
            }
            steps {
                sh 'Going Ahead with Deployment'
            }
        }
        stage('Deploment') {
            steps {
                sh 'sudo cp target/JenkinsWar.war /var/lib/tomcat9/webapps/'
            }
        }
    }
}
