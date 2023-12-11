pipeline {
    agent any
    stages {
        stage('Checkout') {
            steps {
                git url: 'https://github.com/Alikhan034/aws-assignment.git', branch: 'main'
            }
        }
        stage('Build') {
            steps {
                echo 'Building..'
            }
        }
        stage('Test') {
            steps {
                echo 'Testing..'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying..'
                sshPublisher(
                    publishers: [
                        sshPublisherDesc(
                            configName: 'myawsuserver',
                            transfers: [sshTransfer(sourceFiles: '**/*', remoteDirectory: '/home/ubuntu/myapp')],
                            
                        )
                    ]
                )
            }}}}
