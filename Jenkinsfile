node {
    stage ('xterm') {
        // Just some echoes to show the ANSI color.
        stage "\u001B[31mI'm Red\u001B[0m Now not"
        sh "ls"
    }
    stage('Clone sources') {
        git url: 'https://github.com/jfrogdev/project-examples.git'
        sh "printf 'The folder content is:\n'"
        sh "ls"
        sh 'echo "Can you see something?"'
    }
    stage ('Beginning') {
        print "The current environment is: ${env.NODE_ENV}"
        //sh "echo 'There is no content, the folder is empty.'"
        sh "printf 'The pipelines first step.'"
    }
    stage ('Create build output'){
        sh "mkdir -p output"
    }
    stage("Archive build output"){    
        sh "ls | date"
    }
}
