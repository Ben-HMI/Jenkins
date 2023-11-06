pipeline {
    agent any

 parameters {
        string(name: 'NUMBERONE', defaultValue: "4", description: 'The environment name [dev|cert|prod].')
        string(name: 'NUMBERTWO', defaultValue: "4", description: 'The account id on which you will use to do aws cli 
command.')
  }
  
    stages {
        stage('Clone Repo from github') {
            steps {
                git 'https://github.com/darealmc/some_code.git'
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

