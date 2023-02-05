
pipeline {
    agent any
    environment {
       ENV_URL="pipeline.global.com"
       SSH_CRED=credentials('SSH_CRED')
    }

    stages {
        stage('one') {
            steps {
                echo "I am in stage one"
                echo "env_url is ${ENV_URL}"
            }
        }


   stage('two') {
                environment {
                 ENV_URL="stage2.local.com"
                }
            steps {
                echo "I am in stage two"
                echo "env_url is ${ENV_URL}"
            }
        }

stage('three') {
            steps {
                sh '''
                echo I am in stage three
                echo hia there
                echo using jenkins
                echo "env_url is ${ENV_URL}"
                env
                '''
            }
        }
    }
}