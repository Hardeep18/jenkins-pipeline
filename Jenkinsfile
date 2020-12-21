node ('kubepod'){
    def app
    when {
    expression {
        return env.BRANCH_NAME != 'master';
        }
    }
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