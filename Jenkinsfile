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
        mail(subject: 'Test-Mail', body: 'Version : $BUILD_NUMBER ; version1 : $deploy_version', to: 'vinay.kumar@riversand.com', cc: 'vinay.kumar@riversand.com')
      }
    }
  }
}