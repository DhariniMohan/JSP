pipeline {
    agent any
   
    stages {
        stage('Build') {
            steps {
                git url: 'https://github.com/DhariniMohan/JSP.git'
                echo 'Building..'
            }
        }
        stage('maven') {
            steps {
             
                echo 'maven....'
                sh 'mvn -B -DskipTests clean package' 
            }
        }
		stage('Powershell') {
            steps {
             
                 powershell 'Write-Output "Hello!"'
            }
        }
	}
}
