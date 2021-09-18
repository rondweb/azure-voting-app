pipeline {
    agent any

    stages {
        stage('Branch verify') {
            steps {
                echo "$GIT_BRANCH"
            }
        }     

        stage('Creating enviroment') {
            steps {
                sh(script: """
                    cd azure-vote
                    virtualenv env
                    source .env/bin/activate                    
                """)

                // sh(script: 'virtualenv env')
                // sh(script: 'virtualenv env')
                // sh(script: 'conda activate env')                
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
