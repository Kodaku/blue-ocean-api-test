pipeline {
  agent any
  stages {
    stage('API Call') {
      steps {
        httpRequest(url: 'http://localhost:3000/users/1', acceptType: 'APPLICATION_JSON', contentType: 'APPLICATION_JSON', httpMode: 'GET', responseHandle: 'STRING', consoleLogResponseBody: true)
      }
    }

  }
}