// pipeline{
//
//    agent {
//      node {
//        label 'workstation'
//      }
//    }
//
//    triggers { pollSCM('H/2 * * * *') }
//
//    options {
//           ansiColor('xterm')
//        }
//
//     parameters {
//         string(name: 'PERSON', defaultValue: 'Mr Jenkins', description: 'Who should I say hello to?')
//       }
//
//   environment{
//     SAMPLE_URL="example.com"
//   }
//
//    stages{
//
//     stage('one') {
//        input {
//             message "Do You Approve?"
//              ok "Yes"
//         }
//      steps{
//        sh 'echo hello world'
//        sh 'echo hello universe'
//        sh 'echo ${SAMPLE_URL}'
//        sh 'echo PERSON - ${PERSON}'
//       }
//     }
//
//    stage ('two'){
//     when {
//       expression{
//          GIT_BRANCH == "orgin/test"
//         }
//       }
//    steps{
//     sh 'env'
//    }
//    }
//
//   }
//  post {
//    always {
//      sh 'echo post CleanUp steps'
//     }
//   }
//
// }
//

pipeline{
 agent any
 stages {
    stage('parallel'){
     parallel {

   stage('one') {
   steps {
   sh 'echo one'
   }
  }
  stage('two') {
     steps {
     sh 'echo two'
     }
    }
    stage('three'){
       steps {
       sh 'echo three'
       }
       }
      }
    }


