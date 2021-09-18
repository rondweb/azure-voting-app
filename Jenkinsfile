pipeline {
    agent any

    stages {
        stage('Branch verify') {
            steps {
                echo "$GIT_BRANCH"
            }
        }     

        stage('Docker build') {
            steps {
                sh(script: 'docker images -a')
                sh(script: """
                    cd azure-vote
                    docker images -a 
                    docker build -t jenkins-pipeline .
                    docker images -a
                    cd ..
                """)
            }
        }     
    }
    
    
    
}
