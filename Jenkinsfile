pipeline {

  agent any
 
 stages {
    stage('Cloning Git') {
      steps {
        git([url: 'https://github.com/mayankkh1/minikube01.git', branch: 'main'])
 
      }
    }
    
 stage('Deploy to Server') {
      steps{
        
        sh "kubectl apply -k  ."
   
           
      }  
   }

}

}

