node{

    stage('SCM Checkout')
    {
        git credentialsId: '098d0131-e8a3-4de2-b045-8b770b000058', url: 'https://github.com/jesufrancis31/online-shop.git'
    }
    
    stage('Run Docker Compose File')
    {
        sh 'sudo docker-compose build'
        sh 'sudo docker-compose up -d'
    }
  stage('PUSH image to Docker Hub')
    {
      /* withCredentials([string(credentialsId: 'DockerHubPassword', variable: 'DHPWD')]) 
        {
            sh "docker login -u upasanatestdocker -p ${DHPWD}"
        }
        sh 'docker push vardhanns/phpmysql_app'
        */
        //docker.withRegistry( 'https://registry.hub.docker.com', 'DockerHubPassword' ) {
             
             sh 'sudo docker login -u "jesufrancis31" -p "Devops019@" docker.io'
             //sh 'sudo docker push upasanatestdocker/mysql'
             //sh 'sudo docker push upasanatestdocker/job1_web1.0'
             sh 'sudo docker push jesufrancis31/edurekha-onlineshopping-prod_web:latest'
            // sh 'docker push upasanatestdocker/mysql'
          
    }
}
