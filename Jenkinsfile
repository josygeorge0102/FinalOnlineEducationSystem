
pipeline{
  agent any  
  stages {

        stage ('checkout') {
            steps {
                git 'https://github.com/josygeorge0102/OnlineEducationSystem.git'
            }
        }
      
       stage ('Docker Compose Push') {
            steps {                         
                    sh 'docker login oesdemo.azurecr.io -u OESDemo -p /nmSJE7Z1LVEQBhCXPPFr8Q52dNnzKrf'
                    sh'docker-compose push'          
            }
        }
      
  }
}
