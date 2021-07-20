pipeline{

	agent any

	tools{
		maven 'Maven 3.6.1'
	}

	stages{
		stage('build'){
			echo 'compile maven app'
			sh 'mvn compile'
		}

		stage('test'){
			echo 'test maven app'
			sh 'mvn clean test'
		}

		stage('package'){
			echo 'package maven app'
			sh 'mvn package -DskipTests'
		}
	}

	post{
    		always{
        		echo 'This pipeline is completed..'
    		}
  	}
}
