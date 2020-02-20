pipeline {
    agent {
        dockerfile{
            filename 'Dockerfile.build'
            dir 'build'
            additionalBuildArgs  '--build-arg version=1.0.2'
            args '-v /tmp:/tmp'
        }
    }
    stages {
        stage('build') {
            steps {
                sh './gradlew build'
            }
        }
    }
}