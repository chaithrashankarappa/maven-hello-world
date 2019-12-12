pipeline {
    agent any
    tools {
        maven 'M3'
        
           }
    stages {
    
         // stage('Checkout')

                    // {

                       //git branch: 'master',  url: 'https://github.com/macagua/example.java.helloworld.git'

                    // }

        stage ('Initialize') {
            steps {
                   git branch: 'master',  url: 'https://github.com/macagua/example.java.helloworld.git'
                sh '''
                    echo "PATH = ${PATH}"
                    echo "M2_HOME = ${M2_HOME}"
                '''
                  }
                           }

        stage ('Build') {
            steps {
                sh 'mvn -Dmaven.test.failure.ignore=true install' 
                }
            
                        }
    }
}
