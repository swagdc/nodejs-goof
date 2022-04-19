pipeline {
         agent any
         stages {
                 stage('Checkout') {
                 steps {
                     echo 'Checking out code from git'
                 }
                 }
                stage('Scan') {
                    snykSecurity organisation: 'good_demo', projectName: 'goof_demo_snyk', severity: 'medium', snykInstallation: 'Please define a Snyk installation in the Jenkins Global Tool Configuration. This task will not run without a Snyk installation.', snykTokenId: 'goof', targetFile: 'package.json'
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