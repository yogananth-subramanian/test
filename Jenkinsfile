pipeline {
    agent any
    parameters {
        choice(name: 'server', choices: ['master', 'worker'], description: 'Pick something')
        booleanParam(name: 'DEBUG_BUILD', defaultValue: true, description: '')
    }

    stages {
        stage('Hello') {
            steps {
                echo 'Hello World'
                echo "${params.server}"
                echo "${params.DEBUG_BUILD}"
                sh '''
                
                echo $server
                '''
                build(job: 'worker', parameters: [string(name: 'server', value:"${params.server}")] )

            }
        }
    }
}
