pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                sh 'echo "Hello World"'
                sh '''
                    echo "Multiline shell steps works too"
                    cd /home
                    ls -lah
                '''
                //sh 'find / 2> /dev/null | grep encrypt'
                sh 'sudo apt-get -y purge git; sudo apt-get -y autoremove'
                sh ' sudo /usr/bin/apt-get -y install git'
                sh '''
                    mkdir /home/jenkins/gitrepository
                    chmod 777 /home/jenkins/gitrepository
                    cd /home/jenkins/gitrepository
                    git clone https://github.com/zaphodbeeblebox/test
                '''
                
            }
        }
    }
}
