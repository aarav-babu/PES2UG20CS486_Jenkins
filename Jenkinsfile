pipeline{
  agent any
  stages{
    stage('Build'){
      steps{
        sh 'make -C main'
      }
    }
    stage('Test'){
      steps{
        sh 'g++ main.cpp -o main'
        sh 'output=$(./example)'
        sh 'echo "$output"'
      }
    }
    stage("Deploy'){
          steps{
            sh 'echo "Deploy Stage"'
          }
    }
  }
post {
        always {
            echo 'Pipeline completed'
        }
        failure {
            echo 'Pipeline failed'
        }
    }
}          
          
          
