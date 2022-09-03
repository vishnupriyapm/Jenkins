pipeline {
    agent any

    stages {
        stage('pipeline test') {
            steps {
                script{
                sh "echo hostnamectl"
                sh "echo This is Pipeline Job"
                if(env.JOB_NAME=="Declarative-pipeline")
                {
                    echo "Job Name Correct"
                }
                else{
                    echo "Job Name wrong"
                }}
            }
        }
        stage('second stage') {
            steps {
                sh "echo hostnamectl"
                sh '''echo Build Number=$BUILD_NUMBER
                echo Job Name=$JOB_NAME
                echo Job URL= $JOB_URL'''
                
            }
        }
}
}

