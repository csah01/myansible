pipeline{
    agent any
    stages{
        stage('SCM Checkout'){
            steps{
                git branch: 'main', url: 'https://github.com/csah01/myansible'
            }
        }
        stage('Execute Playbook'){
            steps{
                ansiblePlaybook credentialsId: 'privatekey', 
                disableHostKeyChecking: true, 
                installation: 'myansible', 
                inventory: 'dev.inv', 
                playbook: 'playbook1.yml'
            }
        }
    }
}
