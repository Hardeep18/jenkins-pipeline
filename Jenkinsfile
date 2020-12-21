node ('kubepod'){
    def app

    stage('Clone repository') {
          /* Let's make sure we have the repository cloned to our workspace */

        checkout scm
    }

    stage('check branch') {
          when{
             branch 'Devlop'
        }
        echo "Hello Developer"
        }


    stage('Deploy to k8s cluster'){
        agent { 
                label 'k8s'
                }
                steps {
                    checkout scm
                    echo "hello k8s"
                }

    }


}