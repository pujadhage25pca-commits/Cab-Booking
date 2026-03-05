pipeline {
    agent any

    stages {

        stage('Checkout') {
            steps {
                git branch: 'main',
                    url: 'https://github.com/pujadhage25pca-commits/Cab-Booking.git'
            }
        }

        stage('Build') {
            steps {
                echo 'No build step required for static project'
            }
        }

        stage('Archive Artifacts') {
            steps {
                archiveArtifacts artifacts: '**/*.html, **/*.js, **/*.css', fingerprint: true
            }
        }

                stage('Deploy') {
            steps {
                echo "Deploying project..."
                bat 'echo Deployment done'
            }
        }
    }
}
