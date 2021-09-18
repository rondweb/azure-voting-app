pipeline {
    agent any

    stages {
        stage('Branch verify') {
            steps {
                echo "$GIT_BRANCH"
            }
        }     

        stage('Creating conda enviroment') {
            steps {
                sh(script: 'conda create --name env python=3.9 -y')
                sh(script: 'conda activate env')                
            }
        }   

        // stage('Docker build') {
        //     steps {
        //         sh(script: 'docker images -a')
        //         sh(script: """
        //             cd azure-vote
        //             docker images -a 
        //             docker build -t jenkins-pipeline .
        //             docker images -a
        //             cd ..
        //         """)
        //     }
        // }     
    }  
}
