pipeline{
    tools{
        jdk 'myjava'
        maven 'mymaven'
    }
	agent any
      stages{
           stage('Checkout with git'){
              steps{
		 echo 'cloning..'
                 git 'https://github.com/RayItern/JUNECLASSPRO1.git'
              }
          }
          stage('Compile with mvn1'){
              steps{
                  echo 'compiling..'
                  sh 'mvn compile'
	      }
          }
          stage('CodeReview with mvn'){
              steps{
		    
		  echo 'codeReview'
                  sh 'mvn pmd:pmd'
              }
          }
          
          stage('Package with mvn'){
              steps{
                  sh 'mvn package'
              }
          }
      }
}
