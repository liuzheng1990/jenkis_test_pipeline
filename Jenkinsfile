pipeline {
    agent { dockerfile true }
    stages {
        stage('Hello') {
            steps {
                sh 'python --version'
                sh 'python hello.py'
            }
        }
        stage("Work") {
        	steps {
        		sh 'python workload.py'
        	}
        }
        stage("Bye") {
        	steps {
        		sh 'python bye.py'
        	}
        }

    }
}