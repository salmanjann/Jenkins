pipeline{
    agent any

    parameters{
        booleanParam(name: 'DEPLOY', defaultValue: true, description:'Deploy this build?')
    }
    stages{
        stage('Build'){
            steps{
                echo 'Building the application'
            }
        }
        stage('Test'){
            steps{
                echo 'Testing the application'
            }
        }
        stage('Deploy'){
            when{
                expression{
                    return params.DEPLOY == true
                }
            }
            steps{
                echo 'Deploy the application'
            }
        }
    }
}