// pipeline {
//     agent any
//     stages {
//         stage('Build') {
//             steps {
//                 sh 'echo "Hello World"'
//                 sh '''
//                     echo "Multiline shell steps works too"
//                     ls -lah
//                 '''
//             }
//         }
//     }
// }


pipeline {
    agent any
    tools { nodejs "nodejs_lim"}
    stages {
        // stage('Prepare') {
        //     steps {
        //         script {
        //             git branch: 'main', url: 'https://github.com/luckylimanman/cypress_code.git'
        //         }
        //     }
        // }
        stage('Build') {
            steps {
                // cleanWs()
                sh '''
                npm install
                node index.js
                '''
                sh 'echo "Hello World"'
            }
        }
    }
}
    // post {
    //     success {
    //         sh 'sudo git clean -fdx'
    //     }
    //     failure {
    //     sh 'sudo git clean -fdx'
    //     mail to: 'mandli@redhat.com',
    //          subject: "jenkins learn fail",
    //          body: "Something is wrong"
    // }
    // }
