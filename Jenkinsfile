pipeline {
    agent any
	

    stages {
        stage('git repo & clean') {
            steps {
                bat "rmdir /s /q Building-REST-API-Website-CodingWithSonu-"
	  	bat "git clone https://github.com/Mrsonurai/Building-REST-API-Website-CodingWithSonu-.git"
		bat "mvm clean -f Building-REST-API-Website-CodingWithSonu-"
            }
        }
        stage('install') {
            steps {
                bat "mvm install -f Building-REST-API-Website-CodingWithSonu-"
            }
        }
        stage('test') {
            steps {
                bat "mvm test -f Building-REST-API-Website-CodingWithSonu-"
            }
        }
        stage('package') {
            steps {
                bat "mvm package -f Building-REST-API-Website-CodingWithSonu-"
            }
        }
    }
}
