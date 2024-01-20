def displayBranchName() {

    String branch_name = env.BRANCH_NAME
    print(branch_name)
    // 
    if ( branch_name == 'dev' ) {
        print('running the dev env config')
    }
    else if( branch_name == 'test' ) {
        print( 'running test env' )
    }
    else if (branch_name == 'main'){
        print('running production...')
    }
    else{
        print ('i am at feature branchh')
    }
        

}

pipeline {
    agent any
    options {
        // Timeout counter starts AFTER agent is allocated
        timeout(time: 1, unit: 'SECONDS')
    }

    stages {
        stage('build') {
            steps {
                script{
                    displayBranchName()
                }
            }
        }
    }
}