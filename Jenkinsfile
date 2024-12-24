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
        stage('Переход в папку с выгруженным репозиторием роли') {
            steps {
                sh '/home/jenkins/jenkins_agent/workspace/Declarative pipeline'
            }
        }
        stage('Запускаем molecule test') {
            steps {
                sh 'molecule test'
            }
        }
    }
}
