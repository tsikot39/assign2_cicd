pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo 'Installing dependencies...'
                sh 'npm install'
                sh 'npm run build'
            }
        }
        stage('Test') {
            steps {
                echo 'Running tests...'
                sh 'npm test -- --watchAll=false'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying to Netlify...'
                sh 'npm install -g netlify-cli'
                sh 'netlify deploy --prod --site $ee7c4e09-4b9c-41de-a388-aa13f482734d --auth $nfp_fEVrjR4WA2TZckKKCV8fgYRXT9NWQTLWb8c0'
    }
}
    }
}