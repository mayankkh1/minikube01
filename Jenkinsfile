pipeline {

  agent any
 
stages {
    
           stage('Deploy to Server') {
           steps{
        
                   sh "kubectl apply -k  /home/ubuntu/data/minikube01/. "
   
           
                }  
           }

       } 

}    



