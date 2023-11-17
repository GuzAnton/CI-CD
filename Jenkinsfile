pipeline{
    agent any
    tools {
        maven 'MAVEN3'
        jdk 'JDK8'
    }
    environment{
        SNAP_REPO = 'vpofile-snapshot'
        NEXUS_USER = 'admin'
        NEXUS_PASS = '1'
        RELEASE_REPO = 'vprofile-release'
        CENTRAL_REPO = 'vpro-maven-central'
        NEXUSIP = '172.31.18.47'
        NEXUSPORT = '8081'
        NEXUS_LOGIN = 'nexuslogin'
        NEXUS_GRP_REPO = 'vrpo-maven-group'
    }

    stages {
        stage('Build'){
            steps{
                sh 'mvn -s settings.xml -DskipTests install'
            }
        }
    }
}