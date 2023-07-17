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
              sh 'ls' 
              sh 'export PATH=$PATH:$HOME/.local/bin'
              sh 'ansible-playbook -v playbook.yaml' 
            }
        }

    }
}
