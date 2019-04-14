pipeline {
    agent { dockerfile true }
    stages {
        stage('Build docker image') {
            when { 
                branch 'master'
            }
            steps {
                sh  'node --version'
            }
        }
    }

}
