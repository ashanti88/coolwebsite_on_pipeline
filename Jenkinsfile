pipeline {
    agent any
    triggers {
         cron('* * * * *')
    }     
    stages{
        stage("GitClone"){
            steps{
              git 'git@github.com:ashanti88/coolwebsite_on_pipeline.git'
            }

        }
    
        stage("Copy file wo Web"){
            steps{
                sh "cp -f index.html /var/www/html/index.html"
            }
        }
        stage("Test"){
            steps{
                sh "echo Test"
            }
        } 
    }
}
