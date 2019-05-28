pipeline{

deleteDir()

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

    }
}

