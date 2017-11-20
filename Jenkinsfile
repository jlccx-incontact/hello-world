node {
    stage ('Beginning') {
        steps
        {
            //sh "echo 'There is no content, the folder is empty.'"
            sh "printf 'The pipelines first step.'"
        }
    }
    stage ('Create build output'){
        sh "mkdir -p output"
    }
    stage("Archive build output"){    
        sh "ls | date"
    }
}
