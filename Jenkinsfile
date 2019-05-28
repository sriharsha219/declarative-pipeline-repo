pipeline{

agent any

stages{

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
sh "mvn install"
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

