pipeline {
    agent any
    stages {
        stage('build') {
            steps {
                bat 'echo Hello world'
            }
        }
    }
    post {
        always {
            echo 'post-always cleanup'
        }
        success {
            echo 'success cleanup'
        }
        failure {
            echo 'failure cleanup'
        }
        unstable {
            echo 'unstable cleanup'
        }
        changed {
            echo 'changed cleanup'
            echo 'this will only run if the state of the pipeline has changed (e.g. was previously failing but is now successful)'
        }
    }
}