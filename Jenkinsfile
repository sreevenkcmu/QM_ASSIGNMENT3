pipeline {
    agent any
        stage("Build-and-Archrive") {
            steps {
                sh './mvnw package'
            }
            post {
                success {
                    junit '**/target/surefire-reports/TEST-*.xml'
                    archiveArtifacts 'target/*.jar'
                }
            }
        }
    }
