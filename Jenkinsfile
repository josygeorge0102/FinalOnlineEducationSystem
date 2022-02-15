
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

 //        }
         stage ('docker build') {
            steps {
                sh 'docker-compose build'
           }
       }
      
       stage ('Docker Compose Push') {
            steps {                         
                   
                    sh'docker-compose push'          
            }
        }
      
  }
}
