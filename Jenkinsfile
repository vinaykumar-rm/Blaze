pipeline {
  agent any
  parameters  {
    choice(name: 'choice',
      choices: 'I1\nI2\nI3\nI4',
    description: 'please select an instance')

    string(name: 'version',
    description: 'Provide version number')
  }
  stages {
    stage('MailTest') {
      steps{
        echo 'User Choices'
        echo "Instane Name  : ${params.choice}"
        echo "Version Number  : ${params.version}"
      }
    }
  }
}