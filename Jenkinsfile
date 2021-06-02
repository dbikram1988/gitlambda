pipeline {
  agent any
 
  stages {
    stage('Invole Lambda Test Runner') {
      steps {
        lambdaTestRunner branch: 'main', command: 'npm run coverage', functionName: 'localTest', region: 'us-east-1', repoUri: 'https://github.com/dbikram1988/gitlambda/blob/main/processPDF/localTest.js', s3Bucket: 'sam-jenkins-demo-us-east-1-bikram', storeToS3: ''
      }
    }
   
  }
}
