 pipeline {
 
 	//tool name: 'maven', type: 'maven'
 	
 	//def mvnHome = tool name: 'maven', type: 'maven' 
    
    
    agent any

 	stages {
 	
        stage('SCM Checkout') {
            steps {
               
               
               //checkout([$class: 'GitSCM', branches: [[name: '*/master']], doGenerateSubmoduleConfigurations: false, extensions: [], submoduleCfg: [], userRemoteConfigs: [[credentialsId: 'e3170388-caf7-4486-b50a-2ff070d7017f', url: 'https://github.com/TanumayDhar/DevopsTest1.git']]])
                git "https://github.com/TanumayDhar/devSample.git"
                
            }
        }
        stage('Build') {
            steps {
             
          
       			echo 'Building the application...'
                
                
            }
        }
        stage('Integration Test') {
            steps {
            
            	
           //bat (/mvn clean test/)
           bat 'mvn test'  
               //readFile 'DevopsSelenium\\pom.xml' 
           
            //bat label: '', script: 'C:\\PROGRA~2\\apache-maven-3.6.3\\bin\\mvn -Dmaven.test.failure.ignore=true clean package'
 
            //bat label: '', script: 'C:\\PROGRA~2\\apache-maven-3.6.3\\bin\\mvn clean org.jacoco:jacoco-maven-plugin:prepare-agent install -Dmaven.test.failure.ignore=false'  
              
                echo 'Test and Deploying in server...'
            }
        }
    }
}
 
 
