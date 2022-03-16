pipeline {
    agent any
    
    tools {
        nodejs 'NodeJS'
    }

    stages {
        stage('Install') { 
            steps {
                echo 'Installing packages...'

                sh 'npm install' 
            }
        }

        stage('Create .npmrc') { 
            steps {
                sh '''
                    cat > .npmrc << EOL
                    email=ioanainsuratelu@yahoo.com
                    //npm.pkg.github.com/:_authToken=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
                    @madalina1:registry=https://npm.pkg.github.com
                    EOL
                '''
            }
        }
    }
}