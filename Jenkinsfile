pipeline {
    agent any
    tools { 
        maven 'Maven' 
    }
    stages {
        stage('Build') {
            steps {
                sh 'mvn clean install -DskipTests=true'
            }
        }
        stage('Unit Test') {
            steps {
                sh "mvn test -Dtest=AppTest"
            }
        }
        stage('Integration Test') {
            steps {
                echo "Integration Test"
            }
        }
        stage('Deploy') {
            steps {
                // sh "mvn -B deploy"
                // sh "mvn -B release:prepare"
                // sh "mvn -B release:perform"
                // deploy using kubernetes - kubectl
                 echo "Deploy to prod"
            }
        }
    }
}
