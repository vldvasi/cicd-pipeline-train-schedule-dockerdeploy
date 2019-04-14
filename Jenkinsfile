pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                echo 'Running build automation'
                sh './gradlew build --no-daemon'
                archiveArtifacts artifacts: 'dist/trainSchedule.zip'
            }
        }
        stage('Build docker image') {
            when { 
                branch 'master'
            }
            agent { dockerfile true }
            steps {
                sh  'node --version'
            }
        }        
    }
}
