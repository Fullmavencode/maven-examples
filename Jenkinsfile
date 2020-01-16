node {
   
   stage('Code checkout') { // for display purposes
     git credentialsId: 'GitID', url: 'https://github.com/Fullmavencode/maven-examples.git'  
   }
   stage('Build') {
    withMaven(jdk: 'java_1.8', maven: 'maven3.6.1') {
      sh 'mvn clean compile'
    } 
   }
   stage('Test') {
    withMaven(jdk: 'java_1.8', maven: 'maven3.6.1') {
      sh 'mvn test'
    }
   }
  stage('Code Analysis') {
   //withMaven(jdk: 'JDK-1.8', maven: 'Maven-3.6.1') {
   //   sh 'mvn sonar:sonar'
   // }
    
   }
   stage('Package') {
   
    withMaven(jdk: 'java_1.8', maven: 'maven3.6.1') {
      sh 'mvn package'
    }
   }
   stage('Deploy to Dev') {
   
    
   }
   
} 
   
