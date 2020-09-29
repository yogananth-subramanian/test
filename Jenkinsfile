pipeline {
    agent any
    parameters {
        choice(name: 'server', choices: ['master', 'worker'], description: 'Pick something')
    }

    stages {
        stage('Hello') {
            steps {
                echo 'Hello World'
                echo "${params.server}"
                echo "${params.server}"
                sh '''
                
                echo $server
                '''
                build(job: 'worker', parameters: [string(name: 'server', value:"${params.server}")] )

            }
        }
    }
}
