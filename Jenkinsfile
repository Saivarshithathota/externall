pipeline {
    agent any
    stages{
        stage('Build'){
            steps{
                bat 'docker build -t myapp .'
            }
        }
        stage('Run image'){
            steps{
                bat 'docker run -d -p 5000:5000 --name mycontainer myapp'
        }
        }
    }
        post{
            success{
                echo 'Build and run successful!'
            
        }Failure{
            echo 'Build or run failed!'
        }
        }
}