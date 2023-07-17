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
              sh 'sudo chmod 700 runsed.sh'
              sh '/bin/sh runsed.sh'
              sh 'export PATH=$PATH:$HOME/.local/bin ; ansible-playbook -v -i inventory.yaml playbook.yaml'
            }
        }

    }
}                                                                                                                                                            

