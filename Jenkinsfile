pipeline {
    agent any
    stages {
        stage('code clone') {
            steps {
                git 'https://github.com/jyo111/myapp-ansible.git'
            }
        }
        stage('execute ansible') {
            steps {
                ansiblePlaybook credentialsId: 'ansible-new', disableHostKeyChecking: true, installation: 'ansible2', inventory: 'dev.inv', playbook: 'apache.yml'
            }
        }
    }
}
