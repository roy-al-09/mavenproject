pipeline {
  agent any

  stages {
    stage ('scm checkout') {
      steps {
        git branch: 'master', url: 'https://github.com/roy-al-09/mavenproject.git'        // script generated from Pipeline Syntax 
      }
    }

    stage ('execute unit test framework') {
      steps {
        withMaven(globalMavenSettingsConfig: '', jdk: 'JAVA_HOME', maven: 'MAVEN_HOME', mavenSettingsConfig: '', traceability: true) {
        sh 'mvn test'     // script generated from Pipeline Syntax
        }
      }	
    }
  }
}
