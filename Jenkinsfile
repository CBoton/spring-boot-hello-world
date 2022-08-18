Jenkinsfile (Declarative Pipeline)
pipeline {
    agent { docker { image 'docker.io/boton318/spring-boot-hello-world' } }
    stages {
        stage('build') {
            steps {
                sh 'mvn --version'
            }
        }
    }
}