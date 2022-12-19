pipeline{    

    agent any
    stages {
        
        stage("Build") {
            agent any
            steps {
                bat 'mvn clean package'
            }
          }
    }
}
