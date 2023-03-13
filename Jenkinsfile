pipeline {
    agent any
    stages {
        stage('Source') {
            steps {
                dir('vector-role') {
                    git branch: 'master', credentialsId: '0ed4dcfd-6cd3-47c0-bfcc-b01f0149a411', url: 'git@github.com:ivanmanokhin/vector-role.git'
                }           
            }
        }
        stage('Molecule Test') {
            steps {
                sh 'molecule test'
            }
        }
        stage('Clean up') {
            steps {
                deleteDir()
            }
        }
    }
}
