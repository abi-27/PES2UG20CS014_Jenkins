pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                sh 'g++ temp.cpp -o temp'
                 build job: 'PES2UG20CS014-1', wait: false
                 echo 'Build Successful.'
            }
        }

        stage('Test') {
            steps {
                sh 'cat temp.cpp'
                echo 'Test Stage Successful.'
            }
        }

        stage('Deploy') {
            steps {
               
                echo 'Deploy Stage Successful.'
            }
        }
    }

    post {
        failure {
            
                echo 'Pipeline Failed.'
          
        }
    }
}
