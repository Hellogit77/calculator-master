pipeline {
    agent {
        label 'generic'
    } //agent
    stages {
        stage("Setup script") {
            steps {
                sh """
                    sudo yum install -y python36
                    sudo pip3 install --upgrade pip
                    sudo pip3 install pytest
                """
            } //steps
        } //stage
        stage("Run unit tests") {
            steps {
                sh """
                    sudo python3 -m pytest
                """
            } //steps
        } //stage
    } //stages
//    post {
//        always {
//            sh """
//                sudo pip3 uninstall pytest -y
//            """
//        } //always
//    } //post
} //pipeline