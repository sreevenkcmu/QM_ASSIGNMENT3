pipeline {
    agent any
    stages {
        stage("Build-and-Archrive") {
            steps {
                sh 'mvn package'
            }
            post {
                success {
                    junit '**/target/surefire-reports/TEST-*.xml'
                    archiveArtifacts 'target/*.jar'
                }
            }
        }
    }
}