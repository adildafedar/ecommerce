pipeline {
    agent any

    stages {
        stage("Build") {
            steps {
                echo "Building E-Commerce Website"
                bat "npm run build"
            }
        }

        stage("Automated Testing") {
            steps {
                bat "npm test"
            }
        }

        stage("Code Quality Check") {
            steps {
                bat "npm run lint"
            }
        }

        stage("Deployment") {
            steps {
                bat "if not exist deployment mkdir deployment"
                bat "copy index.html deployment/index.html"
                echo "Website deployed to deployment folder"
            }
        }
    }
}