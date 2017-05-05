node {

    stage('Clone From Git') {
    sh 'git pull origin pull/$CHANGE_ID/head'
    }
    
    stage('Test Script') {
    sh 'sh test.sh'
    }
    }
