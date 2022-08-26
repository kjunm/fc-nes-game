pipeline {
    agent {
        docker {
            image 'maven:3.3-jdk-8'
        }
    }

    environment {
        ALICLOUD_ACCESS = 'default'
        ALICLOUD_ACCESS_KEY_ID     = credentials('jenkins-alicloud-access-key-id')
        ALICLOUD_ACCESS_KEY_SECRET     = credentials('jenkins-alicloud-access-key-secret')
    }

    stages {
        stage('Setup') {
            steps {
                sh 'scripts/setup.sh'
            }
        }
    }
}