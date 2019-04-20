pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        echo 'Building..'
        sh 'touch build && rm -r build && mkdir -p build && cd build && cmake -DCMAKE_BUILD_TYPE=Debug .. && make'
      }
    }
    stage('Test') {
      steps {
        echo 'Testing..'
        sh 'cd build && make test'
      }
    }
  }
}
