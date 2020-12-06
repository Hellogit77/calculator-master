pipeline {
    agent {
        label 'generic'
    } //agent
    stages {
        stage("Setup script") {
            steps {
                sh """
                    yum install -y python36
                    pip3 install --upgrade pip
                    pip3 install pytest
                """
            } //steps
        } //stage
        stage("Run unit tests") {
            steps {
                sh """
                    python3 -m pytest
                """
            } //steps
        } //stage
    } //stages
    post {
        always {
            sh """
                pip3 uninstall pytest -y
            """
        } //always
    } //post
} //pipeline