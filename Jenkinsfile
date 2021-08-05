pipeline {
    agent any
	

    stages {
        stage('git repo & clean') {
            steps {
//                 bat "rmdir /s /q Building-REST-API-Website-CodingWithSonu-"
	  	bat "git clone https://github.com/Mrsonurai/Building-REST-API-Website-CodingWithSonu-.git"
		bat "mvn clean -f Building-REST-API-Website-CodingWithSonu-"
            }
        }
        stage('install') {
            steps {
                bat "mvn install -f Building-REST-API-Website-CodingWithSonu-"
            }
        }
        stage('test') {
            steps {
                bat "mvn test -f Building-REST-API-Website-CodingWithSonu-"
            }
        }
        stage('package') {
            steps {
                bat "mvn package -f Building-REST-API-Website-CodingWithSonu-"
            }
        }
    }
}
