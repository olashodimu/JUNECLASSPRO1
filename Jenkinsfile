pipeline{
    tools{
        jdk 'myjava'
        maven 'mymaven'
    }
	agent any
      stages{
           stage('Checkout'){
              steps{
		 echo 'cloning..'
                 git 'https://github.com/RayItern/JUNECLASSPRO1.git'
              }
          }
          stage('Compile maven'){
              steps{
                  echo 'compiling..'
                  sh 'mvn compile'
	      }
          }
          stage('CodeReview maven'){
              steps{
		    
		  echo 'codeReview'
                  sh 'mvn pmd:pmd'
              }
          }
          
          stage('Package maven'){
              steps{
                  sh 'mvn package'
              }
          }
      }
}
