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
        stage('main') {

        echo "Hello main"
        }
    } 

}