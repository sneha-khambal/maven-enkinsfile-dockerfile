pipeline{
agent any
stages{
stage('git checkout'){
steps{
git(credentialsId: 'GITHUB_ID', url: 'https://github.com/sneha-khambal/maven-enkinsfile-dockerfile')

}}
stage('Mvn package'){
  steps{
    def mvnHome = tool name: 'maven', type: 'maven'
    def mvnCMD  = "${mvnHome}/bin/mvn"
    sh "${mvnCMD} clean package"
 echo 'packaged'
  }
 }


}}

 
