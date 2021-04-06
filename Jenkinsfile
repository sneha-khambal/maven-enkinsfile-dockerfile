pipeline{
agent any
stages{
stage('git checkout'){
steps{
git(credentialsId: 'GITHUB_ID', url: 'https://github.com/sneha-khambal/maven-enkinsfile-dockerfile')

}}
stage('Mvn package'){
  def mvnHome = tool name: 'maven', type: 'maven'
    def mvnCMD  = "${mvnHome}/bin/mvn"
  steps{
    
    sh "${mvnCMD} clean package"
 echo 'packaged'
  }
 }


}}

 
