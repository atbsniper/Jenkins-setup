flag = true

pipeline {
agent any
  tools {
maven "Maven"}
  environment { NEW_VERSION = '1.3.0'
              }
stages {
stage('Build') {
steps {
echo 'Building..'
echo "Building version${NEW_VERSION}"
bat "nvm install"
// Here you can define commands for your build
}
}
stage('Test') {
steps {
echo 'Testing..'
// Here you can define commands for your tests
}
}
stage('Deploy') {
steps {
echo 'Deploying....'
// Here you can define commands for your deployment
}
}

}
}
