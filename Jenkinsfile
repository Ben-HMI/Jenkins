@Library('github.com/releaseworks/jenkinslib') _

pipeline {
    agent {
        docker {
            label 'docker-agent-alpine'
            image 'jenkins/agent'
    }
}
    parameters {
    string(name: 'NUMBERONE', defaultValue: "4"       , description: 'The environment name [dev|cert|prod].')
    string(name: 'NUMBERTWO', defaultValue: "4"       , description: 'What should I say?')

    }
    stages {
        stage('Clone Repo from github') {
            steps {
                git 'https://github.com/Ben-HMI/Jenkins.git'
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


