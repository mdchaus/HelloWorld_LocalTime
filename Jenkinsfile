pipeline{
    agent any

    tools {
         maven '/usr/bin/mvn'
         jdk '/usr/bin/java'
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
