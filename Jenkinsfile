 pipeline{
 agent any
 stages{
 stage('code checkout'){
  steps{
       git branch: 'main', credentialsId: 'nit', url: 'https://github.com/bhaskarlinuxgithub/jenkins-ansible.git'
       }
 }
 stage('Execute Ansible'){
  steps{
       ansiblePlaybook credentialsId: 'pipe', disableHostKeyChecking: true, installation: 'ansible', inventory: 'dhost.inv', playbook: 'apache.yml'
       
      }
    }
}
}
