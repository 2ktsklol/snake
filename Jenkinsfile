node ('ubuntu') {
    def app
    stage('Cloning Git') {
       checkout scm
    }

    stage('Build-and-Tag') {
       app = docker.build("2ktsklol/snake")
    }
    stage('Pull-image-server') {
        sh "docker-compose down"
        sh "docker-compose up -d"
    }
}
