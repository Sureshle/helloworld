pipeline 
{
    agent {
    node {
        label 'Maven'
        
    }
    }
    stages {

        stage('Build') {

            steps {
withMaven(jdk: 'JAVA', maven: 'maven') 
             {
sh'mvn clean install'
}
            }
        }
                   
            }
            
}
