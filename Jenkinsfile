pipeline {

    agent any
    
    stages {
        stage('Build') {
            steps {
                sh './gradlew assemble'
            }
        }
        stage('Test') {
     	    steps {
     	        sh './gradlew check'
     	    }
        }
        stage('Deploy') {
            steps {

            }
        }
    }

    post {
         always {
             archive 'build/libs/*.jar'           
         }
    }
}
