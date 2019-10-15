pipeline {
    agent { dockerfile true }
    stages {
    	stage('setup') {
    		steps {
    			echo 'JENKINS setup stage...'
    			sh 'pwd'
    			sh 'ls'
    			sh 'pip install -r requirements.txt'
    		}
    	}
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