pipeline { 
    agent any 
    stages {
        stage('Build') { 
            steps { 
               bat "mvn clean package"
            }
        }
        stage('Test'){
            steps {
               echo "TEST1"
            }
        }
        stage('Deploy') {
            steps {
                echo "TEST2"
            }
        }
    }
}