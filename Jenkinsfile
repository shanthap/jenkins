stage('MyStep') {
    steps {
        echo 'Deploying MyStep'
        script {

            env.NUMBER.split(',').each {
               build job: 'jenkinsfile-demo', parameters: [string(name: 'NUMBER', value: "$it")], wait: false
            }
        }
    }
}
