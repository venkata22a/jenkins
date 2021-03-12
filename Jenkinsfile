pipeline{
 
  agent any
  
  stages{
    stage("build"){
      steps{
      echo "build stage2"
      }
    }
    stage('Load') {
    code = load 'test.groovy'
    }
    stage("test"){
     code.example1()
      steps{
      
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
}
