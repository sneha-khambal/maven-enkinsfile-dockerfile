pipeline{
agent any
stages{
stage('git checkout'){
steps{
git(credentialsId: 'GITHUB_ID', url: 'https://github.com/sneha-khambal/maven-enkinsfile-dockerfile')

}}
stage('Mvn package'){
  
  steps{
    sh "mvn clean package"
 echo 'packaged'
  }
 }
  stage('build docker image'){
    steps{
      sh 'docker build  -t  sneha1997/my-app:2.0.0.0'
    }


}}

 
