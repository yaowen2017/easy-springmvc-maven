pipeline {
   agent any

   stages {
      stage('pull code') {
         steps {
            checkout([$class: 'GitSCM', branches: [[name: '*/master']], doGenerateSubmoduleConfigurations: false, extensions: [], submoduleCfg: [], userRemoteConfigs: [[credentialsId: 'a1d1e2f0-3126-4b52-8642-2776b47099f0', url: 'https://github.com/yaowen2017/easy-springmvc-maven.git']]])
         }
      }
      
      stage('build project') {
         steps {
            sh label: '', script: 'mvn clean package'
         }
      }
      
      stage('publish project') {
         steps {
            echo 'publish project'
         }
      } 
      
   }
}
