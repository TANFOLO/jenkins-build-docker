node {
    def app

    stage('Clone'){
        checkout scm
    }
    
    stage('Build image'){
        app = docker.build("xavki/nginx")
    }
    stage('Run image'){
        docker.image('xavki/nginx').withRun('-p 8083:80') {c -> 
        
            bat 'docker ps'
            bat 'curl localhost'
        }
    }
}