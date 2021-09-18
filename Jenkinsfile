// pipeline {
//     agent any

//     stages {
//         stage('Branch verify') {
//             steps {
//                 echo "$GIT_BRANCH"
//             }
//         }     

//     pipeline {
//         agent any
//         stages {
//             stage('Unit tests') {
//                 steps {
//                 sh '''
//                     conda create --yes -n condaTest python=3.9
//                     source activate condaTest                    
//                 '''
//                 }
//             }
//     }
//     // post {
//     //     always {
//     //         sh 'conda remove --yes -n ${BUILD_TAG} --all'
//     //     }
//     // }
// }

//         // stage('Creating enviroment') {
//         //     steps {
//         //         sh(script: """
//         //             cd azure-vote
//         //             pwd
//         //             virtualenv env
//         //             pwd
//         //             source env/bin/activate                    
//         //         """)

//         //         // sh(script: 'virtualenv env')
//         //         // sh(script: 'virtualenv env')
//         //         // sh(script: 'conda activate env')                
//         //     }
//         // }   

//         // stage('Docker build') {
//         //     steps {
//         //         sh(script: 'docker images -a')
//         //         sh(script: """
//         //             cd azure-vote
//         //             docker images -a 
//         //             docker build -t jenkins-pipeline .
//         //             docker images -a
//         //             cd ..
//         //         """)
//         //     }
//         // }     
//     }  
// }


pipeline {
    agent any
    stages {
        stage('Unit tests') {
            steps {
            sh '''
                conda create --yes -n env python=3.9
                source activate env
            '''
            }
        }
    }
    post {
        always {
            sh 'conda remove --yes -n env --all'
        }
    }
