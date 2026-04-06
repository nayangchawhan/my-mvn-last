pipeline{
  agent any

  tools{
    maven 'Maven'
  }

  stages{
    stage('checkout'){
      steps{
        git branch:'master', url:'https://github.com/nayangchawhan/my-mvn-last'
      }
    }

    stage('build'){
      steps{
        sh 'mvn clean package'
      }
    }

    stage('compile'){
      steps{
        sh 'mvn compile'
      }
    }

    stage('test'){
      steps{
        sh 'mvn test'
      }
    }

    stage('run application'){
      steps{
        sh 'java -jar target/my-mvn-last-1.0-SNAPSHOT.jar'
      }
    }
  }

  post{
    success{
      echo 'Application run successefully'
    }

    failure{
      echo 'Failure'
    }
  }
}
