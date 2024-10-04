pipeline {
  agent {
    docker {
      image 'node:16.14.2'
      label 'docker'
    }
  }

  environment {
    HOME = "${env.WORKSPACE}"
  }
      
    stages {
        stage('Push to GitHub') {
          when {
            branch pattern: 'main', comparator: 'GLOB'
    	    expression { return isBuildSuccess() }
          }
          steps {
            sh 'git checkout main'
            
            // push changes to GitHub
            authGit 'cesmarvin', "push -f https://github.com/scm-manager/tsconfig main --tags"
         }
        }
    }
}

boolean isBuildSuccess() {
  return currentBuild.result == null || currentBuild.result == 'SUCCESS'
}

void authGit(String credentials, String command) {
  withCredentials([
    usernamePassword(credentialsId: credentials, usernameVariable: 'AUTH_USR', passwordVariable: 'AUTH_PSW')
  ]) {
    sh "git -c credential.helper=\"!f() { echo username='\$AUTH_USR'; echo password='\$AUTH_PSW'; }; f\" ${command}"
  }
}
