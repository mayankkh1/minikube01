pipeline {


  environment {
 
    imagename = "mak1993/nodeapp01"
    registryCredential = 'mak1993'
    dockerImage = ''
  }

  agent any

  stages {
    stage('Cloning Git') {
      steps {
        git([url: 'https://github.com/mayankkh1/minikube01.git', branch: 'main'])
 
      }
    }

 stage('Building image') {
      steps{
        script {
          dockerImage = docker.build imagename
        }
      }
    }
stage('Deploy Image') {
      steps{
        script {
          docker.withRegistry( '', registryCredential ) {
            dockerImage.push("$BUILD_NUMBER")
            
          }
        }
      }
    }

stage('Deploy app') {
            steps{
                script {
                    
              
                    kubernetesDeploy(configs: "nodeapp.yaml", kubeconfigId: "kubernetes", enableConfigSubstitution: "true")

        }
      } 
   }
 stage('Deploy to Server') {
      steps{
        
        sh "kubectl apply -k ."
   
           
      }  
   }

}

}

