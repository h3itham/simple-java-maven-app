pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                script {
                    // Run Docker commands within a Docker container
                    docker.image('maven:3.9.6-eclipse-temurin-17-alpine').inside {
                        // Run Maven build commands inside the Docker container
                        sh 'mvn -B -DskipTests clean package'
                    }
                }
            }
        }
    }
}


