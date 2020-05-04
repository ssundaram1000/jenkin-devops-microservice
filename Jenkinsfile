
// SCRIPTED PIPELINE
// node {
//     echo "Build"
//     echo "Test"
//     echo "Integration Test"
// }


// DECLARATIVE
pipeline {
    //agent { docker { image 'maven:3.6.3' } }
    agent { docker { image 'node:14.1.0' } }
    stages {
        stage('Build') {
            steps {
//                 sh "mvn --version"
                sh "node --version"
                echo "Build"
            }
        }
        stage('Test') {
            steps {
                echo "Test"
            }
        }
        stage('Integration Test') {
            steps {
                echo "Integration Test"
            }
        }
    }
    post {
        always {
            echo 'I am awesome. I run always'
        }
        success {
            echo 'I run when you are successful'
        }
        failure {
            echo 'I run when you fail'
        }
        // Unstable - When a test failure happens
        // Changed - When status of a build changes
    }
}
