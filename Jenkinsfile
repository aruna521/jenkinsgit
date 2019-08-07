node('master')
{
  stage('cont download')
{
    git 'https://github.com/aruna521/jenkinsgit.git'
}
stage('cont build')
{
    sh label: '', script: 'mvn package'
}
stage('cont deployment')
{
sh label: '', script: 'scp /home/ubuntu/.jenkins/workspace/scripted/webapp/target/webapp.war ubuntu@172.31.29.56:/var/lib/tomcat8/webapps/testwebapp.war'
}
stage('cont testing')
{
    git 'https://github.com/aruna521/jenkinsgit.git'
    sh label: '', script: 'echo "testing passed "'
}
stage('cont delivery')
{
sh label: '', script: 'scp  /home/ubuntu/.jenkins/workspace/scripted/webapp/target/webapp.war ubuntu@172.31.30.136:/var/lib/tomcat8/webapps/prodwebapp.war'
}
}
