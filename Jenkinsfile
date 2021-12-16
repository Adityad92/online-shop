node{

    stage('SCM Checkout')
    {
        git url: 'https://github.com/Adityad92/online-shop.git'
    }
    
    stage('Run Docker Compose File')
    {
        sh 'docker-compose build'
        sh 'docker-compose up -d'
    }
  stage('PUSH image to Docker Hub')
    {
      /* withCredentials([string(credentialsId: 'adicop49', variable: 'flemfjT2@')]) 
        {
            sh "docker login -u adicop49 -p ${flemfjT2@}"
        }
        sh 'docker push Adityad92/online-shop'
        */
        //docker.withRegistry( 'https://registry.hub.docker.com', 'DockerHubPassword' ) {
             
             sh 'sudo docker login -u "adicop49" -p "Zephyr@17" docker.io'
             //sh 'sudo docker push adicop49/mysql'
             //sh 'sudo docker push adicop49/job1_web1.0'
             sh 'sudo docker push adicop49/job1_web2.0'
            // sh 'docker push adicop49/mysql'
          
    }
}
