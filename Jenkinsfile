pipeline {
  agent any
  stages {
    stage("Clean Up"){
      steps{
        deleteDir()
      }
    }
    stage("Clone Repo"){
      steps {
        bat "git clone https://github.com/CBoton/spring-boot-hello-world.git"
      }
    }
    stage("Build"){
      steps {
        dir("spring-boot-hello-world") {
          bat "mvn clean install"
        }
      }
    }
    stage("Test") {
      steps {
        dir("spring-boot-hello-world") {
          bat "mvn test"
        }
      }
    }
    stage("Run") {
        steps {
          dir("spring-boot-hello-world") {
            bat "mvn spring-boot:run"
        }
      }
    }
  }
}


