
pipeline{
  agent any  
  stages {

        stage ('checkout') {
            steps {
                git 'https://github.com/josygeorge0102/FinalOnlineEducationSystem.git'
            }
        }
//         stage("Fix the permission issue") {

//             agent any

//             steps {
//                 sh "sudo chown root:jenkins /run/docker.sock"
//                 }

//         }
        stage ('docker build') {
            steps {
                sh 'sudo docker-compose build'
            }
        }
      
       stage ('Docker Compose Push') {
            steps {                         
                    sh 'docker login oesdemo.azurecr.io -u OESDemo -p /nmSJE7Z1LVEQBhCXPPFr8Q52dNnzKrf'
                    sh'sudo docker-compose push'          
            }
        }
      
  }
}
