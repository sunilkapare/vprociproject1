pipeline {
     agent any
     tools {
        maven "maven3"
        jdk "OracleJDK8"

     }

     environment {
        SNAP_REPO = 'vprofile-snapshot'
        NEXUS_USER = 'admin'
        NEXUS_PASS = 'admin@1'
        RELEASE_REPO = 'vprofile-release'
        CENTRAL_REPO = 'vpro-maven-central'
        NEXUS_IP = '172.31.50.80'
        NEXUS_PORT = '8081'
        NEXUS_GRP_REPO = 'vpro-maven-groupe'
        NEXUS_LOGIN = 'nexuslogin' 
     }

     stages {
        stage('Build'){
            steps {
                sh 'mvn -s setting.xml -DskipTests install'
            }
        }

     }   
}