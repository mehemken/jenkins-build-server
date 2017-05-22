pipeline {
    node any
    triggers {
        pollSCM('*/2 * * * *')
    }
    stages {
        stage('Notify') {
            steps {
                sh 'echo Building...'
                emailext (
                    subject: "Hello from Jenkins",
                    body: """<p>Howdy.</p>
                    <p>'${env.JOB_NAME} [${env.BUILD_NUMBER}]'</p>
                )
            }
        }
    }
}
