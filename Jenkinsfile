pipeline { 
    agent any 
    stages {
        stage('Build') { 
            steps { 
                "mvn clean package"
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