// properties([pipelineTriggers([githubPush()])])

pipeline {
    agent {
        label 'jenkins2_vm_agent'
    }

    stages {
        stage('Clone') {
            steps {
                echo 'Hello World - not githubPUsh() properties'
                sh 'hostname'
                // checkout([$class: 'GitSCM', branches: [[name: '*/main']], extensions: [], userRemoteConfigs: [[credentialsId: 'jenkins_vm jenkins user', url: 'git@github.com:fimtestuvw/jenkins_test.git']]])
                // git credentialsId: 'jenkins_vm jenkins user', url: 'git@github.com:fimtestuvw/jenkins_test.git'
                git credentialsId: 'jenkins_vm jenkins user', url: 'git@github.com:fimtestuvw/jenkins_test.git', branch: 'main'
            }
        }
        
        stage('List Files'){
            steps {
                pwd()
                sh 'ls -alt'
            }
        }
    }
}
