pipeline{
    agent any
    environment{
        BRANCH = 'Main'
    }

    stages{
        stage("Step1"){
            steps{
                echo 'STEP 1'
                sh 'printenv'
            }
        }

        stage("Step2"){
            when {
                expression { BRANCH ==~ '/Main' }
            }
            steps{
                echo 'STEP 2'
            }
        }

         stage("Step3"){
            when{
                expression { BRANCH ==~ '/{Release}/'}
            }
            steps{
                echo 'STEP 3'
            }
        }
    }
}