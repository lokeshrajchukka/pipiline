pipeline {

    agent any

    stages {
        stage('Compile') {
            steps {
                echo "Compiling the Code.........."
                bat "mvn compile"
            }
        }
        stage('Testing') {
            steps {
                echo "Testing the Code.........."
                bat "mvn test"
            }
        }
        stage('Packaging') {
            steps {
                echo "Packaging the Code.........."
                bat "mvn package" 
            }
        }
     }
  } 
