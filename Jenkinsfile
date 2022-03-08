pipeline {
     agent any
     stages{
          stage("git") {
             step(git branch: 'main', url: 'https://github.com/csowji/cmrproject.git')
          }
         stage("maven build"){
            step('mvn clean install')
         }
         stage("build image"){
            steps
             ("docker build -t cmrproject-repo/myapp:1.0 .")
             ("docker run -dt cmrproject-repo/myapp:1.0 /bin/bash")
             ("docker tag cmrproject-repo/myapp:1.0 dharanig746/cmr-repo:1.0")
             ("docker push sowji19999/cmr-repo:1.0")
         }
    }
}
