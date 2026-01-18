pipeline {
    agent any
    
    parameters {
        string(
            name: 'TERRAFORM_PATH',
            defaultValue: './terraform',
            description: 'Шлях до Terraform-коду'
        )
        booleanParam(
            name: 'AUTO_APPROVE',
            defaultValue: false,
            description: 'Прапорець для auto-apply'
        )
        choice(
            name: 'ENVIRONMENT',
            choices: ['dev', 'stage', 'prod'],
            description: 'Оточення (dev, stage, prod)'
        )
    }
    
    stages {
        stage('Checkout') {
            steps {
                echo "Checking out code..."
                checkout scm
            }
        }
        
        stage('Terraform Init') {
            steps {
                echo "Запуск Terraform з параметрами"
                echo "Environment: ${params.ENVIRONMENT}"
                echo "Terraform Path: ${params.TERRAFORM_PATH}"
                echo "Auto Approve: ${params.AUTO_APPROVE}"
                sh '''
                    echo "Running terraform init..."
                    echo "This is a placeholder for terraform init"
                '''
            }
        }
        
        stage('Terraform Plan') {
            steps {
                sh '''
                    echo "Running terraform plan..."
                    echo "This is a placeholder for terraform plan"
                '''
            }
        }
        
        stage('Terraform Apply') {
            when {
                expression { params.AUTO_APPROVE == true }
            }
            steps {
                sh '''
                    echo "Running terraform apply..."
                    echo "This is a placeholder for terraform apply"
                '''
            }
        }
    }
    
    post {
        always {
            echo "Pipeline completed for branch: ${env.BRANCH_NAME}"
        }
    }
}

