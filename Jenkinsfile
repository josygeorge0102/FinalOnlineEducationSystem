
pipeline{
  agent any  
  stages {

        stage ('checkout') {
            steps {
                git ''
            }
        }
        stage ('docker build') {
            steps {
                sh 'docker-compose build'
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
