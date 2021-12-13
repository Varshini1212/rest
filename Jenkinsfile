node{
  
  stage('code build'){
    git 'https://github.com/Varshini1212/rest.git'
  }
  stage('build') {
    def mvnHome = tool name: 'maven3', type: 'maven'
    sh "${mvnHome}/mvn clean install"
  }
  stage('deploy to tomcat') {
    sh "cp -r /var/lib/jenkins/workspace/rest-webapp/target/restaurant.war /opt/apache-tomcat-9.0.56/webapps/"
   }
}
