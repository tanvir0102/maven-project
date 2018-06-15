pipeline {
    agent any

    stages { 
        stage ('Compile Stage') {

            steps{ 
                withMaven(maven : 'mavem_3_3_9') {
                  sh 'mvn Clean Compile'
              }
           }
       }
    
       stage ('Testing Stage') {

         steps {
            withMaven(maven : 'maven_3_3_9') {
                sh 'mvn Test'
              }
           }
       }
    
       stage ('Deployment Stage') {

         steps {
            withMaven(maven : 'maven_3_3_9') {
                sh 'mvn Deploy'
              }
           }
       }

      