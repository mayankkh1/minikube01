pipeline {

  agent any
 
    
 stage('Deploy to Server') {
      steps{
        
        sh "kubectl apply -k  /home/ubuntu/data/minikube01/."
   
           
      }  
   }

}



