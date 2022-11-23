ipeline {
    agent any
    options {
        timeout(time: 1, unit: 'HOURS')
    }
    triggers {
        pollSCM('* * * * *')
    }
    stages {
        stage('sourcecode') {
            steps {
                git url: 'https://github.com/Prasadsgithub/Npm-kanna.git', 
                branch: 'master'
            }   
        }
        stage( 'Buildthecode') {
            steps {
                sh 'npm install'
                sh 'npm run build'
            }  
        }
    }
} 