pipeline {
    agent any
    parameters {
        choice(name: 'server', choices: ['worker', 'master'], description: 'Pick something')
    }

    stages {
        stage('Hello') {
            steps {
                echo 'Hello World'
                echo "${paramas.server}"
                sh '''
                
                echo $server
                '''
                
            }
        }
    }
}
