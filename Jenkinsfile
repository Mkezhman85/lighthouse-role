pipeline {
    agent {
        label 'ansible'
    }
    stages {
        stage('Установка ansible-lint yamllint для выполнения molecule') {
            steps {
                sh 'pip install yamllint ansible-lint'
            }
        }
        stage('Проверяем вресию yamllint') {
            steps {
                sh 'yamllint -v'
            }
        }
    }
}
