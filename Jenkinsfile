pipeline {
    agent {
         label 'any' 
        }
    triggers{
        pollSCM ('* * * * *')
    }
    stages {
        stage('clone') {
            steps {
              git url: 'https://github.com/sivamurthy7473/test2.git',
              branch: 'master'
            }
        }

        stage('ansibleplaybook'){
             
            steps(nsibleplaybook) {
                
                sh script: 'cd ansible/tomcat && ansible-playbook -i hosts ubuntu.yaml'
            }

    }
  }
}