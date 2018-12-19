stage('MyStage') {
        steps {
            echo 'Deploying MyStep'
            script {
                def numbers = [:]
                env.NUMBER.split(',').each {
                    numbers["numbers${it}"] = {
                        build job: 'jenkinsfile-demo', parameters: [string(name: 'NUMBER', value: "$it")]
                    }
                }                   
                parallel numbers
            }
        }
    }
