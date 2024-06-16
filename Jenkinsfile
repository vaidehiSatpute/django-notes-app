
pipeline {
    agent any 
    
    stages {
        stage("Clone Code") {
            steps {
                echo "Cloning the code"
                git url: "https://github.com/vaidehiSatpute/django-notes-app.git", branch: "main"
            }
        }
        stage("Build") {
            steps {
                echo "Building the image"
                sh "docker build -t my-node-app ."
            }
        }
        stage("Deploy"){
            steps {
                echo "Deploying the container"
                sh "docker run -it -d -P  my-node-app"
                
            }
        }
    }
}
