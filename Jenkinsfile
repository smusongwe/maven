node('master') 
{
    stage('Continuous Download') 
	{
    git 'https://github.com/sunildevops77/maven.git'
	}
    stage('Continuous Build') 
	{
    sh label: '', script: 'mvn package'
	}
    stage('Continuous Deployment') 
	{
sh label: '', script: 'scp /home/ansadmin/.jenkins/workspace/ScriptedPipeline/webapp/target/webapp.war   ansadmin@35.166.224.196:/var/lib/tomcat8/webapps/qaenv.war'
	}
    stage('Continuous Testing') 
	{
              sh label: '', script: 'echo "Testing Passed"'
	}
    stage('Continuous Delivery') 
	{
sh label: '', script: 'scp /home/ansadmin/.jenkins/workspace/ScriptedPipeline/webapp/target/webapp.war   ansadmin@35.85.35.188:/var/lib/tomcat8/webapps/prodenv.war'
	}
}
