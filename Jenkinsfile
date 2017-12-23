pipeline{

   agent any
   
    tools { 
        maven 'M3' 
        jdk 'JDK8' 
    }
	
   stages {
	stage ('Initialize') {
            steps {
                sh '''
                    echo "PATH = ${PATH}"
                    echo "M2_HOME = ${M2_HOME}"
                '''
            }
        }
       /* stage('Checkout') {
            steps {
                echo 'Checkout..'
                git url: 'file:////opt/git/first.git', branch: 'master'
            }
        }*/
        stage('Compile') {
            steps {
                echo 'Compile..'
                sh "mvn compile"
            }
        }
        stage('Test') {
            steps {
                echo 'Test..'
                sh "mvn test"
            }
        }
    }
}

