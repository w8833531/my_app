pipeline { 
    agent { node { label 'Java' }} 
    options {
        skipStagesAfterUnstable()
    }
    stages {
        stage('---Mvn Clean---') { 
            steps {
                sh 'mvn clean'
            }
        }
        stage('---Mvn Test---'){
            steps {
                sh 'mvn test'
            }
        }
        stage('---Mvn Deploy---') {
            steps {
                sh 'mvn package'
            }
        }
    }
}
