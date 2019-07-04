pipeline {
 	agent any

 	stages {
 		stage('checkout stage') {
 		 	steps {
 		 		checkout scm 
 		 	}
 		}
 		stage('compile stage') {
 			steps {
 				sh ('python buzz/generator.py')
 			}
 		}
 		stage('env creation') {
 			steps {
 				sh ('virtualenv venv')
 			}
 		}
 		stage('install requirements') {
 			steps {i
 				sh ('pip install -r requirements.txt')
 			}
 		}
 		stage('testing the code') {
 			steps {
 				sh ('python -m pytest -v tests/test_generator.py')
 			}
 		}

	} 
}

