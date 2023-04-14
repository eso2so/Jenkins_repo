pipeline {
    agent any
    environment {
        NEW_VERSION = '1.0.0'
        ADMIN_CREDENTIALS = credentials('0792c5cf-4185-46f7-92db-5a48e2b280f0')
    }
    stages {
        stage("build") {
            steps {
                echo 'building the applicaiton...'
                echo "building version ${NEW_VERSION}"
            }
        }
        stage("test") {
            steps {
                echo 'testing the applicaiton...'
            }
        }
        stage("deploy") {
            steps {
                echo 'deploying the applicaiton...'
                echo "deploying with ${ADMIN_CREDENTIALS}"
                sh 'printf ${ADMIN_CREDENTIALS}'
            }
        }
    }
}
