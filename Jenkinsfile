pipeline {
  agent any
  stages {
    stage('API Call') {
      steps {
        httpRequest(url: 'http://localhost:3000/users/1', acceptType: 'APPLICATION_JSON', contentType: 'APPLICATION_JSON', httpMode: 'GET', responseHandle: 'STRING', consoleLogResponseBody: true)
        script {
          def response = httpRequest "http://localhost:3000/users/1"

          pipeline{
            agent any
            stages {
              stage("Print Variable response") {
                steps {
                  echo "Status: ${response.status}"
                  echo "Response: ${response.content}"
                }
              }
            }
          }
        }

      }
    }

  }
}