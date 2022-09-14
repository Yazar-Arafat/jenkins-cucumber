pipeline{

    agent any

    stages {
        
        stage("Build") {
            agent any
            steps {
                sh 'mvn clean package'
            }
          }
        
        stage ('Cucumber Reports') {
            steps {
                cucumber buildStatus: "UNSTABLE",
                    fileIncludePattern: "**/cucumber-reports/cucumber.json",
                    jsonReportDirectory: 'target'
            }
        }
    }
}
