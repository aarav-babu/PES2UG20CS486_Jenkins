pipeline{
  agent any
  stages{
    stage('Build'){
      steps{
        sh 'make -C main'
        build job : 'pes2ug20cs486-1'
      }
    }
    stage('Test'){
      steps{
        sh 'output=$(make main)'
        sh 'echo "$output"'
      }
    }
    stage('Deploy'){
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
          
          
