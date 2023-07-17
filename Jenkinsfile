pipeline {
    agent any
    parameters {
        booleanParam(name: 'Refresh',
                    defaultValue: false,
                    description: 'Read Jenkinsfile and exit.')
		    }
    stages {
        stage('run app') {
            steps {
              sh 'pwd'
              sh 'whoami'
              sh 'ls'
              sh 'sed -i "s/localhost/all/g" playbook.yaml'
              sh 'sed -i "s/172\.31\.44\.207/54.78.97.167/g" inventory.yaml'
              sh 'sed -i "s#/home/ubuntu/.ssh/myKey#/home/jenkins/eu-west-1-personal.pem#g" inventory.yaml'
              sh 'export PATH=$PATH:$HOME/.local/bin'
              sh 'export PATH=$PATH:$HOME/.local/bin ; ansible-playbook -v -i inventory.yaml playbook.yaml' 
            }
        }

    }
}
