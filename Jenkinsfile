pipeline {
    agent {
        docker {
            image 'maven:3-alpine' 
            args '-v /root/.m2:/root/.m2' 
        }
    }
    stages {
        stage('pull code') {
            steps {
                git credentialsId: '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', url: 'https://github.com/kobe1314/situationAnalysis.git'
         }
      }
        stage('Build') { 
            steps {
                sh 'mvn -B -DskipTests clean package' 
            }
        }
    }
}