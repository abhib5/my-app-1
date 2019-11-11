pipeline {
    agent any
    stages {
        stage('clean repo') {
            steps {
                bat "rmdir /s /q my-app-1"
                bat "git clone https://github.com/abhib5/my-app-1.git"
                bat "mvn clean -f my-app-1"
            }
        }
        stage('Test') {
            steps {
                bat "mvn test -f my-app-1"
                
            }
        }
        stage('Deploy') {
            steps {
                bat "mvn package -f my-app-1"
                
            }
        }
    }
}
