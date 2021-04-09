pipeline{
agent any
stages{
stage('git checkout'){ 

}}
stage('Mvn package'){
  
  steps{
    sh "mvn clean package"
 echo 'packaged'
  }
 }
  stage('build docker image'){
    steps{
      sh 'docker build  -t  sneha1997/my-app:2.0.0.0 .'
    }


}

  stage('push to dockerHub'){
  steps{
      withCredentials([string(credentialsId: 'dockr_pswd', variable: 'docker_pswd')]) {
    sh "docker login -u sneha1997 -p ${docker_pswd}"
}
      sh 'docker push sneha1997/my-app:2.0.0.0'} 
  
  }
   
}
}
 
