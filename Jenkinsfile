pipeline {
    agent any 
    //stages {
        // stage( 'Clone repository') {
        //     steps {
        //         checkout ([$class: 'GitSCM',
        //          branches: [[name: '*/main']], 
        //          userRemoteConfigs: [[url: 'https://github.com/Gayathri-Nettem/PES1UG21CS378_Jenkins.git']]])
        //     }
        // }
stage( 'Build') {
    steps {
        build 'PES2UG21CS378-1'
        sh 'g++ main.cpp -o output'
        }
}
stage('Test') {
    steps {
        sh './output'
}
}
stage ('Deploy') {
    steps {
        echo 'deploy'
}
}
}
post{
failure{
    error 'Pipeline failed'
}
｝
}
