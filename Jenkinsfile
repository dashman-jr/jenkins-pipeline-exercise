pipeline {
    agent any

    stages {
        stage('greetings') {
            steps{
                echo 'Holla Mundos!'
            }
        }
        stage('Preparation') {
            steps{
                echo 'Preparing...'
            }
        }
        stage('Build') {
            steps{
                echo 'Building...'
                ./gradlew clean test jar
            }
        }
        stage('Results') {
            steps{
                echo 'Preparing results...'
                junit '**/build/test-results/test/TEST-*.xml'
            }
        }
    }
}
