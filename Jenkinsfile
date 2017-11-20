pipeline {
    agent { docker 'node:6.3' }
    stages {
        stage('build') {
            steps {
                sh 'echo "hello world at " | date'
                sh 'npm --version'
            }
        }
        stage('unit-test'){
            sh 'npm --version'
        }
    }
    post {
        always {
            echo 'This step always run.'
        }
        success {
            echo 'This step is going to run only If the pipeline finished successfully.'
        }
        failure {
            echo 'This code just run on a failed pipeline'
        }
        unstable {
            echo 'This message is showed only when the pipeline execution was marked as unstable.'
        }
        changed {
            echo 'This will run just if the state of the pipeline has changed'
            printf 'For example, If the pipeline was previously failing and now it was executed successfully.'
        }
    }
}
