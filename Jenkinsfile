pipeline {
    agent any
    tools {
        maven "MAVEN3"
        jdk "OracleJDK8"
    }
    
    environment {
        SNAP_REPO = 'Maven-snapshot'
		NEXUS_USER = 'admin'
		NEXUS_PASS = 'admin@123'
		RELEASE_REPO = 'Jenkins-ci'
		CENTRAL_REPO = 'Jenkins-central'
		NEXUSIP = '172.31.83.102'
		NEXUSPORT = '8081'
		NEXUS_GRP_REPO = 'Maven-group'
        NEXUS_LOGIN = 'nexuslogin'
    }

    stages {
        stage('Build'){
            steps {
                sh 'mvn -s settings.xml -DskipTests install'
            }
        }
    }
}