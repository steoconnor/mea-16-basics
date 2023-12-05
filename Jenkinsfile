pipeline {

    agent any

    stages {

        stage('Echoing') {

            steps {

                sh '''
                 echo "Hi there"
                 pwd
                 echo "Inside shell block"
                '''

            }

        }

        stage('Run script') {

            steps {

                sh '''
                 sh ./run.sh
                '''

            }

        }

        }

        post {
            always {
                archiveArtefacts '*.zip'
            }
        }

}