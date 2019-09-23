pipeline { 
    agent { node { label 'Java' }} 
    options {
        skipStagesAfterUnstable()
    }
    stages {
        stage('clean') { 
            steps {
                sh 'mvn clean'
            }
        }
        stage('Test'){
            steps {
                sh 'mvn test'
            }
        }
        stage('Deploy') {
            steps {
                sh 'mvn package'
            }
        }
    }
}
