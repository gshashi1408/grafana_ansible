pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                sh 'rm -rf grafana'
                sh 'git clone https://github.com/gshashi1408/grafana_ansible.git'
            }
        }
        stage('Deploy grafana') {
            steps {
                sh 'ansible-playbook grafana.yml -i inventory/hosts'
            }
        }
    }
}
