pipeline{

agent any

stages{

stage('Project-Creation'){

steps{
sh "cd /home/ec2-user/"
sh "pwd" > PWD
echo "Creating sample maven-webapp"
sh "mvn archetype:generate -DgroupId=Web-App -DartifactId=Declarative-Webapp -DarchetypeArtifactId=maven-archetype-webapp -DinteractiveMode=false"
sh "A sample maven webapp is created in $PWD"
    }
}

stage('Build'){

steps{
sh "cd /home/ec2-user/Declarative-Webapp"
sh "pwd" > PWD
echo "Building sample maven-webapp"
sh "mvn clean install"
sh "Project build is completed in $PWD"
    }
}

}
