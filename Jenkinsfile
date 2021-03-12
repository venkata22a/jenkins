def sg = ''
pipeline{
 
  agent any
  
  stages{
    stage("build"){
      steps{
      echo "build stage2"
      }
    }
   
  stage('Load') {
   steps {
     script{
      sg = load 'test.groovy'
     }
   }
   }
    stage("test"){
     
     steps{
      script{
      sg.example1()
     }
      echo "test stage"
      }
    }
    stage("deploy"){
      steps{
      echo "deploy stage"
      }
    }
    stage("validate"){
      steps{
      echo "validate stage"
      }
    }
  }
 post { 
        always { 
            echo 'I will always say Hello again!'
        }
    }
}
