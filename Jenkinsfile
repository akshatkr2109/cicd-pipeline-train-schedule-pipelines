pipeline {
    agent any

    stages {
        stage("Execute Gradle Build") {
            steps {
                ./gradlew build --no-daemon
            }
        }
    }

    post {
        success {
            archiveArtifacts artifacts: 'dist/trainSchedule.zip', fingerprint: true
        }
    }
}