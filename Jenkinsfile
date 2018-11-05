node('master') 
{
     
    stage('ContinuousDownload-Feature1') 
    {
       git 'https://github.com/selenium-saikrishna/maven.git'
    }
    stage('ContinuousBuild-Feature1')
    {
        sh 'mvn package'
    }
    stage('ContinuousDeployment-Feature1')
    {
        sh 'scp /home/vagrant/.jenkins/workspace/ScriptedPipeline/webapp/target/webapp.war vagrant@10.0.0.5:/var/lib/tomcat7/webapps/feature1.war'
    }
    stage('ContinuousTesting-Feature1')
    {
        git 'https://github.com/selenium-saikrishna/FunctionalTesting.git'

    }
}

