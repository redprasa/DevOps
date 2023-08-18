pipeline {
    agent 'any'
    stages {
        stage('git-clone') {
            steps {
            sh '''
            rm -rf *
            echo "Welcome to svm pipeline stage"
            git clone "https://github.com/redprasa/devops.git"
            '''
            }
        }
        stage('tools-test') {
            steps {
            sh '''
            echo "testing the tools"
            java -version
            echo "$JAVA_HOME"
            mvn --version
            echo "$MAVEN_HOME"
            '''
            }
        }
        stage('mvn clean') {
            steps {
            sh '''
            ls -a -ll
            pwd
            cd devops
            ls -a -ll
            mvn clean
            '''
            }
        }
        stage('mvn compile') {
            steps {
            sh '''
            ls -a -ll
            pwd
            cd devops
            ls -a -ll
            mvn compile
            '''
            }
        }
        stage('mvn test') {
            steps {
            sh '''
            ls -a -ll
            pwd
            cd devops
            ls -a -ll
            mvn test
            '''
            }
        }
        stage('mvn sonar:sonar') {
            steps {
            sh '''
            ls -a -ll
            pwd
            cd devops
            ls -a -ll
            mvn sonar:sonar
            '''
            }
        }
        stage('mvn package') {
            steps {
            sh '''
            ls -a -ll
            pwd
            cd devops
            ls -a -ll
            mvn package
            '''
            }
        }
        stage('Deploymetn to requreid servers') {
            steps {
            sh '''
            ls -a -ll
            pwd
            cd devops
            ls -a -ll
            echo "please add the required Aritfaictoery etc servers here as per realtime"
            '''
            }
        }
        stage('Testing or QA team scripts') {
            steps {
            sh '''
            ls -a -ll
            pwd
            cd devops
            ls -a -ll
            '''
            }
        }
        stage('jfrod deployment') {
            steps {
            sh '''
            echo "welcome to maven stage"
            pwd
            ls -a -ll
            curl -uadmind:Password123 -T /c/Users/pknrs/.jenkins/workspace/pipeline-cicd/devpos/target/vracademy-1.0.0.jar "http://localhost:8081/artifactory/devopsbackup/"
            ls -ll
            '''
            }
        }
}
}
