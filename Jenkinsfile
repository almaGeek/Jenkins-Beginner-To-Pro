pipeline{
    agent any // what node or jenkis slave should this run on
    stages {
        stage("Clean Up"){
            steps{
                deleteDir()
            }
        }
        stage("Clone Repo") {
            steps{
                sh "git clone https://github.com/jenkins-docs/simple-java-maven-app.git"
            }
        }
        stage("Build"){
            steps {
                dir("simple-java-maven-app"){
                    sh "mvn clean install"
                }
            }
        }
        stage("test"){
            steps{
                dir("simple-java-maven-app"){
                    sh "mvn test"
                }
            }
        }
    }
}