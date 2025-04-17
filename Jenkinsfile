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

        stage('sonar scan'){
            steps{
                echo '========executing sonar scan========'
                sh 'ls -ltr'
                sh 'sonar-scanner'
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