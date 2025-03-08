pipeline{
    agent any

    tools {
         maven 'Maven 3.9.5'
         jdk 'jdk 17'
    }

    stages{
        stage('checkout'){
            steps{
                checkout([$class: 'GitSCM', branches: [[name: '*/master']], extensions: [], userRemoteConfigs: [[credentialsId: 'github access', url: 'https://github.com/mdchaus/HelloWorld_LocalTime.git']]])
            }
        }
        stage('build'){
            steps{
               bat 'mvn package'
            }
        }
    }
}
