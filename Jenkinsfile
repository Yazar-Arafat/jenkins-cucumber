pipeline{

    agent any

    stages {
        stage ('Cucumber Reports') {
            steps {
                cucumber buildStatus: "UNSTABLE",
                    fileIncludePattern: "**/cucumber-reports/cucumber.json",
                    jsonReportDirectory: 'target'
            }
        }
    }
}
