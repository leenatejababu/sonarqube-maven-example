node {

def IMAGE_NAME = params.IMAGE_NAME
def TAG_NAME = params.TAG_NAME
 def TAG_NAME_Latest = params.TAG_NAME_Latest
 def Jfog_Ip = params.Jfog_Ip
 def Jfog_Port = params.Jfog_Port
 def Repository_Key = params.Repository_Key
 
// def docker_login = params.docker_login
// def Dockerhub_URL = params.Dockerhub_URL

stage('Checkout') {
 git credentialsId: 'Github', url: 'https://github.com/leenatejababu/sonarqube-maven-example.git'
 }


stage('Build') {
    withMaven(jdk: 'JAVA', maven: 'maven') {
        
        println "build is running"
        sh 'mvn clean package'
    }
}

}
