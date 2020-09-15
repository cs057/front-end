pipeline{

    agent any

	tools{
	 maven 'Maven 3.6.3'
        }
	
    stages{
        stage('build'){
            steps{
                echo 'this is build job'
                sh 'npm install'
            }
        }
        stage('test'){
            steps{
                echo 'this is test job'
                sh 'npm test'
            }
        }
        stage('package'){
            steps{
                echo 'this is package job'
                sh 'npm run package'
            }
        }
    }

    post{
        always{
            echo 'this pipeline has completed...'
        }

    }

}
