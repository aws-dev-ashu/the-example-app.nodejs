pipeline{
    
    agent{
        label {
                label 'uat'
                }
            }
    
    stages{
        stage('clone contenful'){
                steps{
                    sh "sudo su"
                    git "https://github.com/aws-dev-ashu/the-example-app.nodejs.git"
                     }
        
                            }
        stage('Deploy contenful'){
                steps{
                    script {
                        sh """
                            docker-compose up -d
                        """
                    }
                    
                }
        
    }                        
        
    }
     post {
        always {
            deleteDir()
        }
    }
}
