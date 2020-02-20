pipeline {
    agent none
    stages {
        stage('build') {
            agent {
                dockerfile{
                    filename 'Dockerfile'
                    dir 'build'
                    additionalBuildArgs  '--build-arg version=1.0.2'
                    args '-v /tmp:/tmp'
                }
            }
            steps {
                sh './gradlew build'
            }
        }
    }
}