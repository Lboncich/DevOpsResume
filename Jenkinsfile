pipeline {
    agent any

    stages{
        stage('deploy to S3'){
            steps{
               sh 'aws s3 cp public s3://lukeresume --recursive'
            }
        }
    }
    post{
        always{
            cleanWs disableDeferredWipeout: true, deleteDirs: true
        }
    }

}