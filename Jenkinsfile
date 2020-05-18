node {
  stage('build & deploy') {
    openshiftBuild bldCfg: 'os-sample-java-web',
      namespace: 'learn2excel',
      showBuildLogs: 'true'
    openshiftVerifyDeployment depCfg: 'os-sample-java-web',
      namespace: 'learn2excel'
  }
  stage('approval (test)') {
    input message: 'Approve for testing?',
      id: 'approval'
  }
    stage('approval (production)') {
    input message: 'Approve for production?',
      id: 'approval'
  }
}