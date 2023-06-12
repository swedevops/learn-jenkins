pipeline{

   agent any {
      node {

      label 'workstation'

      }
   }

   stages{

   stage('one') {

   steps{

    sh 'echo hello world'

   }

   }

  }

  post {
  always{

  sh 'echo post CleanUp steps'
}
  }

}