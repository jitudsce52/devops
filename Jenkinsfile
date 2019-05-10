pipeline {
    agent any

    stages {
        stage("build and deploy on Windows and Linux") {
            parallel {
                stage("ubuntu") {

                    stages {
                        stage("build") {
                            steps {
                                sh "ls -l"
                            }
                        }
                        stage("deploy") {
                            when {
                                branch "master"
                            }
                            steps {
                                echo 'deploy'
                            }
                        }
                    }
                }

                stage("linux") {
                    stages {
                        stage("build") {
                            steps {
                                sh "ps -ef "
                            }
                        }
                        stage("deploy") {
                             when {
                                 branch "master"
                             }
                             steps {
                                sh "ls -l"
                            }
                        }
                    }
                }
            }
        }
    }
}
