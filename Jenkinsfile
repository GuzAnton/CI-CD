pipeline{
    agent any
    tools{
        maven "MAVEN3"
        jdk "JDK8"
    }
    environment{
        SNAP_REPO = 'vprofile-snapshot'
        NESUS_USER = 'admin'
        NEXUS_PASS = '1'
        RELEASE_REPO = 'vprofile-release'
        CENTRAL_REPO = 'vpro-maven-central'
        NEXUS_GRP_REPO = 'vpro-maven-group'
        NEXUSIP = '172.31.18.47'
        NEXUSPORT = '8081'
        NEXUS_LOGIN = 'nexuslogin'
    }
    stages{
        stage("Build"){
            sh 'mvn -s settings.xml -DskipTests install'
        }

    }
}