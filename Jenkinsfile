pipeline {
  agent any
  stages {
    stage('Source') { 
      steps {
	    checkout([$class: 'GitSCM', branches: [[name: '*/master']], doGenerateSubmoduleConfigurations: false, extensions: [], submoduleCfg: [], userRemoteConfigs: [[url: 'https://github.com/saritha1919/jenkins2-course-spring-boot.git']]])
      }
      
      }
    stage('Compile') { 
      tools {
        // Specify Tool Name from your global tool configuration
		jdk 'jdk8'
        maven 'Maven'
      }
      steps {
              powershell 'mvn clean package'
      }
    }
  }
}
