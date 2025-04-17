pipeline{
    agent{
        node{
            label "AGENT-1"
        }
    }
    stages{
        stage('install dependencies'){
            steps{
                echo "========executing A========"
                sh 'npm install'
            }
           
        }
        stage('unit test'){
            steps{
                echo '========executing unit test========'
            }
        }

        
    }
    post{
        always{
            echo "========always========"
        }
        success{
            echo "========pipeline executed successfully ========"
        }
        failure{
            echo "========pipeline execution failed========"
        }
    }
}