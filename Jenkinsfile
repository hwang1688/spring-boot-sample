pipeline {

    agent any
    
    stages {
        stage('Build') {
            steps {
                sh './gradlew clean assemble'
            }
        }
        stage('Test') {
     	    steps {
     	        sh './gradlew check'
     	    }
        }
    }

    post {
         always {
             archive 'build/libs/*.jar'           
         }
    }
}
