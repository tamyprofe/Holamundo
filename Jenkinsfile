groovy
     pipeline {
         agent any
         stages {
             stage('Build') {
                 steps {
                     echo 'Building the application...'
                     sh 'python3 -m py_compile app.py'
                 }
             }
             stage('Test') {
                 steps {
                     echo 'Running tests...'
                     sh 'python3 -m unittest discover -s . -p "*_test.py" || true'
                 }
             }
             stage('Deploy') {
                 steps {
                     echo 'Deploying to test environment...'
                     sh 'cp app.py /tmp/app_deployed.py'
                     sh 'ls -la /tmp/app_deployed.py'
                 }
             }
         }
     }

