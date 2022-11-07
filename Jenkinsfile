pipeline {

  agent any
 
 stages {
    stage('Cloning Git') {
      steps {
        git([url: 'https://github.com/mayankkh1/dockerreactjs.git', branch: 'master'])
 
      }
    }
    
 stage('Deploy to Server') {
      steps{
        
        sh "kubectl delete -k ."
        sh "kubectl apply -k  ."
   
           
      }  

}
