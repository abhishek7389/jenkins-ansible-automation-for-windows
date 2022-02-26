pipeline{
    agent any
    stages{
        stage("SCM Checkout"){
            steps{
                git 'https://github.com/abhishek7389/jenkins-ansible-automation-for-windows'
            }
        }
        stage("Apply Ansible Playbook"){
            steps{
                ansiblePlaybook credentialsId: 'adminuser', disableHostKeyChecking: true, installation: 'Ansible', inventory: 'inventory', playbook: 'playbook.yml'
            }
        }
    }
}
