pipeline{
  agent any
  stages{
    stage('Checkout'){
      steps{
	checkout scm
      }
    }
    stage('Build'){
      steps{
	sh 'echo "Building application.."'
        sh 'python3 --version'
      }
    }
    stage('Test'){
      steps{
	sh '''
	python3 - <<EOF
import calculator
assert calculator.add(2,3)==5
assert calculator.multiply(2,3)==6
assert calculator.subtract(5,2)==3
assert calculator.divide(6,2)==3
print ("All tests passed")
EOF
        '''
      }
    }
    stage('Deploy'){
      steps{
	sh 'echo "Deployement step (dummy for now)"'
      }
    }
  }
}

