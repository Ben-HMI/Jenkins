pipeline {
    agent any

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

