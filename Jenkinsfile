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

           	stage ('Docker')
			{
			 steps
				{
				  sh ' sudo docker build -t tomcat .' 
				}
			}
			stage ('copy')
			{
			 steps
				{
				  sh ' cp /gitlearning/jenkins/helloworld.war /gitlearning/jenkins/workspace/Dockerdeploy/' 
				}
			}
           
			stage ('Push')
			{
				steps
				{
			sh ' docker push sureshle/tomcatdeploy:latest '
				}
			}
			stage ('K8S')
				{
				steps
				{
				sh ' kubectl create -f Deploy.yaml '
				}
				}
        }
            
}
