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

    stages {
        stage('Build') {
            steps {
                git branch: main, url: 'https://gitlab.cee.redhat.com/cplabstests/e2e.git'
                sh '''
                npm install
                node index.js
                '''
                sh 'echo "Hello World"'
            }
        }
    }
    // post {
    //     failure {
    //     mail to: 'mandli@redhat.com',
    //          subject: "jenkins learn fail",
    //          body: "Something is wrong"
    // }
    // }
}