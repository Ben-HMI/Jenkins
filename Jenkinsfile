@Library('github.com/releaseworks/jenkinslib')

pipeline {
    agent any
    parameters {
    string(name: 'NUMBERONE', defaultValue: "4"       , description: 'The environment name [dev|cert|prod].')
    string(name: 'NUMBERTWO', defaultValue: "4"       , description: 'What should I say?')

    }
    stages {
        stage('Clone Repo from github') {
            steps {
                git 'https://github.com/Ben-HMI/Jenkins.git'
                withCredentials([[$class: 'UsernamePasswordMultiBinding', credentialsId: 'aws-key', usernameVariable: 'AWS_ACCESS_KEY_ID', passwordVariable: 'AWS_SECRET_ACCESS_KEY']]) {
                AWS("--region=eu-west-1 s3 ls")
    }
            }

        }
        stage('Build shell script') {
            steps {
                sh '''chmod +x testscript.sh
                bash testscript.sh'''
            }

        }

    }
}

