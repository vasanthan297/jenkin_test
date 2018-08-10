pipeline { 
    agent any 
    stages {
        stage('Build') { 
            steps { 
             //  bat "mvn clean package"
			  echo "TEST1"
            }
        }
        stage('Test'){
            steps {
               echo "TEST2"
            }
        }
        stage('Deploy') {
            steps {
                echo "TEST2"
				bat "cf -v"
				
				  withCfCli(  
						apiEndpoint: 'api.run.pivotal.io',
						skipSslValidation: true, 
						cloudFoundryCliVersion: 'Cloud Foundry CLI (built-in)',
						credentialsId: '36ccbb19-9890-48b3-a392-3479f944abb8',  
						organization: 'bpds', 
						space: 'poc') { 

                        sh 'cf push my-app-name -p target/my-app*.war' (8)

                   }
   
   
				//bat "cf login --skip-ssl-validation -a api.run.pivotal.io -u vasanthan297@gmail.com -p OMhari297!";
				//bat "cf target -o bpds"
				//bat "cf target -s poc"
				//bat "cf push"
				//bat "cf services"
				 echo "Testing OKAY"
            }
        }
    }
}