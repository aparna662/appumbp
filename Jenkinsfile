node('master')
{
   stage('ContinuousDownload')
    {
        git 'https://github.com/intelliqittrainings/maven.git'
    } 
    
    stage('ContinuousBuild')
    {
        sh label: '', script: 'mvn package'
    }
    
    stage('ContinuousDeployment')
    {
        sh label: '', script: 'scp /home/ubuntu/.jenkins/workspace/scriptedpipeline/webapp/target/webapp.war ubuntu@172.31.13.18:/var/lib/tomcat8/webapps/testapp.war'
        }
}

   

