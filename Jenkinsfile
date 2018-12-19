stage('MyStep') {
    steps {
        echo 'Deploying MyStep'
        script {

            env.NUMBER.split(',').each {
               build job: 'Master_Child', parameters: [string(name: 'NUMBER', value: "$it")], wait: false
            }
        }
    }
}
