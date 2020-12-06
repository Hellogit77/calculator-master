pipeline {
    agent {
        label 'generic'
    }
    stages {
        stage("Setup script") {
            steps {
                sh """
                    sudo yum install -y python36
                    sudo pip3 install --upgrade pip
                    sudo pip3 install pytest
                """
            }
        }
        stage("Run unit tests") {
            steps {
                sh """
                    sudo python3 -m pytest
                """
            }
        }
//		stage("Deploy  to another server") {
//			steps {
//				sh """
//				#//	Package into rpm and upload
//				"""
//			}
//		}
        
    } //stages
//    post {
//        always {
//            sh """
//                sudo pip3 uninstall pytest -y
//            """
//        } //always
//    } //post
} //pipeline