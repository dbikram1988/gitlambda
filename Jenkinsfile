pipeline {
  agent any
 
  stages {
    stage('Invole Lambda Test Runner') {
      steps {
        lambdaTestRunner branch: 'main', command: 'npm run coverage', functionName: 'arn:aws:lambda:us-east-1:652488947426:function:modularclmsearch-ProcessPDFFunction-1IAJIYE9HPJL0', region: 'us-east-1', repoUri: 'https://github.com/dbikram1988/gitlambda', s3Bucket: 'sam-jenkins-demo-us-east-1-bikram', storeToS3: ''
      }
    }
   
  }
}
