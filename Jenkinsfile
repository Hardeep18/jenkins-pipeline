node ('kubepod'){
    def app

    stage('Clone repository') {
          /* Let's make sure we have the repository cloned to our workspace */

        checkout scm
    }


    if (env.BRANCH_NAME == "deployment") {                                          
        stage('develop') {

        echo "Hello Developer"
        }
    } else {                                   
        agent { 
                label 'k8s'
                }
                steps {
                    sh 'kubectl --kubeconfig /var/jenkins_home/kube/config get nodes'
                }

    } 

}