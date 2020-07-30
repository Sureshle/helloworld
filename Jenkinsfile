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
           
			stage ('Push')
			{
			steps
			{
			sh ' sudo docker push sureshle/tomcatdeploy:latest
			}
			}
        }
            
}
