pipeline {
  agent any
  stages {
    stage('MailTest') {
      steps {
        sh '''packageversion=$(date +%m%d%y.%H%M)

echo $packageversion${TAG_SUFFIX} > rdp_deploy_version.txt

BUILD_NUMBER=$(cat $KEY_FOLDER_PATH/versionNumber.txt)
deploy_version=$(cat rdp_deploy_version.txt)

echo $BUILD_NUMBER
echo $deploy_version'''
      }
    }
  }
  environment {
    KEY_FOLDER_PATH = '/var/lib/jenkins/keys/'
    KEY_FILE_NAME = 'riversand-east-1.pem'
    REMOTE_SERVER = 'ubuntu@54.210.14.231'
  }
}