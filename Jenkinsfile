pipeline {
     agent any
     stages {
          stage("Clone stage") {
               steps {
                    git 'https://github.com/handuy/nodejs-todolist.git'
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
