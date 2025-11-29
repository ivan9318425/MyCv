pipeline{
    agent any
    environment{
        DEST_DIR="C:\\inetpub\\wwwroot\\myCv"
    }
    stages{
                stage('Checkout scm'){
                    steps{
                            checkout scm
                    }

        }
        stage('Build'){
            steps{
                bat "mkdir ${DEST_DIR}"
            }
            
        }

        stage('Deploy'){
            steps{
                bat "xcopy .\\* ${DEST_DIR}\\ /e /y /h"
            }
        }
    }
}