pipeline{
agent any
stages{
stage('git checkout'){
steps{
git(credentialsId: 'GITHUB_ID', url: 'https://github.com/sneha-khambal/maven-enkinsfile-dockerfile')

}
 stage('Mvn package'){
 sh 'mvn clean package'
 echo "packaged" 
 }
  
}}}

 
