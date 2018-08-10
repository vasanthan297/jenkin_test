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
				bat "cf -v"
				bat "cf login --skip-ssl-validation -a api.run.pivotal.io -u vasanthan297@gmail.com -p OMhari297!";
				bat "cf target -o bpds"
				
            }
        }
    }
}