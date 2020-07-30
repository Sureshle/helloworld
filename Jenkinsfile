pipeline 
{
  agent 
    
 {
    node 
        {
            label 'k8s'
        
        }
    }
    stages 
        {
stage ('copy')
			{
			 steps
				{
				  sh ' cp /gitlearning/jenkins/helloworld.war /gitlearning/jenkins/workspace/Dockerdeploy/' 
				}
			}
		
           	stage ('Docker')
			{
			 steps
				{
				  sh ' sudo docker build -t tomcat .' 
				}
			}
			
           
			stage ('Push')
			{
			steps
			{
				sh 'docker tag tomcat:latest sureshle/tomcatdeploy:latest '
				sh ' docker login --username sureshle --password pass@1234 '
			sh ' sudo docker push sureshle/tomcatdeploy:latest '
			}
			}
        }
            
}
