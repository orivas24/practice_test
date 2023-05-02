pipeline{
    agent any
    environment { 
    	EXECUTE = false
    }
    stages{
        stage('First'){
            steps{
                echo "Updating First Stage" 
            }
        }    
        stage('Second'){
            when {
                expression { EXECUTE == 'false' }
            } 
            steps{
                echo "Updating Second Stage"
            }
        }
        stage('Third'){
             when {
                expression { EXECUTE == 'true' }
            } 
            steps{
                echo "Updating Third Stage"
            }
        }
    }
}
