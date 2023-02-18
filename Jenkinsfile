pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                sh 'g++ -o PES2UG20CS014-1 hello_pipeline.cpp'
                echo "Build Successful."
            }
        }
        stage('Test') {
            steps {
                sh 'g++ hello_pipeline.cpp'
                echo "Test Stage Successfull."
            }
            post {
                failure {
                    echo 'Test Stage Failed.'
                }
              }
        }
       stage('Deploy') {
            steps {
                sh '-o pipeline_exec'
                echo 'Deployed Successfully.'
            }
        }
    }
  
    post {
        always {
            echo 'Pipeline Completed.'
        }
        failure {
            echo 'Pipeline Failed.'
        }
    }
}
