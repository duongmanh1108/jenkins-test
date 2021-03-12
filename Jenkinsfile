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
}
