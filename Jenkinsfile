pipeline{

agent any

stages{


stage('SonarQube Analysis'){

steps{

echo "Sending code for SonarQube analysis"
sh "sonar-scanner -Dsonar.projectKey=Declarative-Pipeline -Dsonar.sources=. -Dsonar.host.url=http://18.191.245.96 -Dsonar.login=73fb4a283811a21ea3cfe95b9930ba698b5072ab"
echo "Project uploaded to SonarQube"
echo "Check results in SonarQube"
input("Do you want to proceed ?")
    }
}

stage('Compile'){

steps{

echo "Compiling sample maven-webapp"
sh "mvn clean compile"
echo "Project compiled"
    }
}

stage('Test'){

steps{

echo "Compiling sample maven-webapp"
sh "mvn clean compile"
echo "Project tested"
    }
}
stage('Package'){

steps{

echo "Packing sample maven-webapp"
sh "mvn package"
echo "Project packed"
    }
}
stage('Install'){

steps{

echo "Installing sample maven-webapp"
sh "mvn install"
echo "Project installed"
    }
}

stage('Deploy'){

steps{

echo "Deploying sample maven-webapp"
sh "mvn deploy"
echo "Project deployed to Nexus repository"
    }
}

  }

post {
        always {
            echo 'One way or another, I have finished'
            deleteDir() /* clean up our workspace */
        }
        success {
            echo 'I succeeeded!'
        }
        unstable {
            echo 'I am unstable :/'
        }
        failure {
            echo 'I failed :('
        }
        changed {
            echo 'Things were different before...'
        }
    }
}

