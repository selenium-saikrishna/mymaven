node('master') 
{
     
    stage('ContinuousDownload-master') 
    {
       git 'https://github.com/selenium-saikrishna/maven.git'
    }
    stage('ContinuousBuild-master')
    {
        sh 'mvn package'
    }
    stage('ContinuousDeployment-master')
    {
        sh 'scp /home/vagrant/.jenkins/workspace/ScriptedPipeline/webapp/target/webapp.war vagrant@10.0.0.5:/var/lib/tomcat7/webapps/qaenv.war'
    }
    stage('ContinuousTesting-master')
    {
        git 'https://github.com/selenium-saikrishna/FunctionalTesting.git'

    }
}

