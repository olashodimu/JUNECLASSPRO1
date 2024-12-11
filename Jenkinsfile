pipeline{
    tools{
        jdk 'ourjava'
        maven 'ourmaven'
    }
	agent any
      stages{
           stage('Checkout with git'){
              steps{
		 echo 'cloning..'
                 git 'https://github.com/tinubu/JUNECLASSPRO1.git'
              }
          }
          stage('Compile with maven'){
              steps{
                  echo 'compiling..'
                  sh 'mvn compile'
	      }
          }
          stage('CodeReview with maven'){
              steps{
		    
		  echo 'codeReview'
                  sh 'mvn pmd:pmd'
              }
          }
          
          stage('Package with maven'){
              steps{
                  sh 'mvn package'
              }
          }
      }
}
