node{
    def mavenHome = tool name: "maven3.6.3"
    stage("check out code"){
        git credentialsId: 'githubcredentials', url: 'https://github.com/pravschevuru/maven-web-app.git'
    }
    stage("maven build"){
        sh "${mavenHome}/bin/mvn clean package"
    }
    stage("Generate SonarQube Report"){
        sh "${mavenHome}/bin/mvn sonar:sonar"
    }
}
