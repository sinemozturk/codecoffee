def displayBranchName() {
    String branch_name = env.BRANCH_NAME
    print(branch_name)
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