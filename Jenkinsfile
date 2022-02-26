pipeline {
   agent any
   stages {
    stage('Checkout') {
      steps {
        script {
           // The below will clone your repo and will be checked out to master branch by default.
           git credentialsId: '', url: 'https://github.com/abhishek7389/jenkins-ansible-automation-for-windows'
           // Do a ls -lart to view all the files are cloned. It will be clonned. This is just for you to be sure about it.
           sh "ls -lart ./*" 
           // print the directory where you're files are copied. 
           sh "pwd"
          }
       }
    }
    stage("Apply Ansible Playbook"){
      steps{
           ansiblePlaybook credentialsId: '', disableHostKeyChecking: true, installation: 'Ansible', inventory: '/etc/ansible/hosts', playbook: '/home/abhishek_sharma_searce_com/playbook.yml'
      }
    }
  }
}
