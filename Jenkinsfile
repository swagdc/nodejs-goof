pipeline {
         agent any
         stages {
                 stage('Checkout') {
                 steps {
                     echo 'Checking out code from git'
                 }
                 }
                 stage('Build') {
                 steps {
                     echo 'Building'
                 }
                 }
                 stage('Test') {
                 parallel { 
                            stage('Unit Test') {
                           steps {
                                echo "Running the unit test..."
                           }
                           }
                           }
                           }
              }
}