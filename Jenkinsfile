pipeline{
    agent any
    tools {
      nodejs 'nodejs16.16.0'
    }
    stages{
        stage('SCM'){
            steps{
                git branch: 'main', changelog: false, poll: false, url: 'https://github.com/jisnarose6y/react-todo-app.git'
            }
        }
        stage('install'){
            steps{
              sh 'npm install'
            }
        }
        stage('build'){
            steps{
                sh 'npm start'
            }
        }
        stage('deploy'){
            
            steps{
                sh 'cp ./build/* /var/www/html/'
            }
            
        }
      
        }
    }
