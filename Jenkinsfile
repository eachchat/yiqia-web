pipeline {
  agent {
    node {
      label 'nodejs'
    }

  }

  environment {
        DOCKER_CREDENTIAL_ID = 'dockerhub'
        GITHUB_CREDENTIAL_ID = 'github-id'
        KUBECONFIG_CREDENTIAL_ID = 'kubeconfig'
        REGISTRY = 'dockerhub.qingcloud.com'
        DOCKERHUB_NAMESPACE = 'eachchat'
        APP_NAME = 'yiqia-web'
        SONAR_CREDENTIAL_ID = 'sonar-token'
        SONAR_HOST_ID = 'sonar-host'
  }
  stages {
    stage('代码拉取') {
      steps {
        git(url: "${env.GIT_URL}", credentialsId: "$GITHUB_CREDENTIAL_ID", changelog: true, poll: false, branch: "${env.GIT_BRANCH}")
      }
    }
    stage('推送镜像') {
      steps {
        container('base') {
          withCredentials([usernamePassword(credentialsId : "$DOCKER_CREDENTIAL_ID" ,passwordVariable : 'DOCKER_PASSWORD' ,usernameVariable : 'DOCKER_USERNAME' ,)]) {
            sh 'echo "$DOCKER_PASSWORD" | docker login $REGISTRY -u "$DOCKER_USERNAME" --password-stdin'
            sh 'docker build -t $REGISTRY/$DOCKERHUB_NAMESPACE/$APP_NAME:$BRANCH_NAME-$BUILD_NUMBER  .'
            sh 'docker push $REGISTRY/$DOCKERHUB_NAMESPACE/$APP_NAME:$BRANCH_NAME-$BUILD_NUMBER'
          }
        }
      }
    }
    stage('显示新镜像') {
      steps {
        echo "新tag: $BRANCH_NAME-$BUILD_NUMBER"
      }
    }
  }
}