
node('windows-agent')
{
    
        stage('---clean---') { 
           
                bat "mvn clean"
            
        }
        stage('---test---') { 
           
                bat "mvn test" 
            
        }
        stage('---package---') { 
           
                bat "mvn package" 
            
        }
}
