pipeline { 
 
 agent any 
 
 stages { 
 
  stage('Clone Repository') { 
   steps { 
    git 'https://github.com/sambhramnaregal/ci-cd-web-app.git' 
   } 
  } 
 
  stage('Build Docker Image') { 
   steps { 
    bat 'docker build -t web-devops-app .' 
   } 
  } 
 
  stage('Run Docker Container') { 
   steps {
 
    bat 'docker run -d -p 8081:80 --name web-container web-devops-app' 
   } 
  } 
 
 } 
 
}