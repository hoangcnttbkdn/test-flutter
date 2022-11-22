pipeline {
    agent any
    stages {
        stage("Clean Build Debug APK") {
            steps {
                sh "cd android"
                sh "./gradlew clean"
            }
        }
        stage("Build Debug APK") {
            steps {
                sh "./gradlew assembleDebug"
            }
        }
    }
    post {
        always {
            archiveArtifacts artifacts: '*/.apk'
        }
    }
}

