#jenkins file
pipeline {
  agent any
  stages {
    stage('Checkout Code') {
      steps {
        git 'https://github.com/your-username/my-webapp.git'
      }
    }
    stage('Deploy') {
      steps {
        sh '''
          sudo mkdir -p /var/www/html
          sudo cp index.html /var/www/html/index.html
        '''
      }
    }
  }
}
