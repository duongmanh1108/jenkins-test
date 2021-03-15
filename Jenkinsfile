pipeline {
     agent any
     stages {
          stage("Clone stage") {
               steps {
                    git 'https://github.com/duongmanh1108/jenkins-test-02.git'
               }
          }
          stage("Build stage") {
               steps {
                    sh 'docker build -t nodejs-todolist .'
               }
          }
     }
     post {
          always {
               emailext body: '${DEFAULT_CONTENT}', subject: '${DEFAULT_SUBJECT}', to: 'duongmanh1108@gmail.com'
          }
     }
}
