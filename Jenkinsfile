pipeline{
    agent any
    stages{
        stage('compile'){
            steps{
                echo "compile start"
                git 'https://github.com/harishk1234/batch6.git'
                sh label: '', script: '''mvn compile'''
                 echo "compile end"
            }
        }
        
        stage('test'){
            steps{
                echo "test start"
                sh label: '', script: '''mvn test'''
                 echo "test end"
            }
        }
        
        stage('deploy'){
            steps{
                echo "deploy start"
                sh label: '', script: '''mvn package'''
                //sh label: '', script: '''ssh -i key user@ip-address'''
                //sh label: '', script: '''cp **/*.war /var/lib/tomcat8/webapps'''
                echo "deploy end"
            }
        }
    }
}
