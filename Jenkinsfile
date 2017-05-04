node {

    stage 'Clone From Git'
    git url: 'https://github.com/sacheen12/testing.git'

    stage 'Run Test on PR'
    def job = hudson.getItem(sshah12/job/hello/)
    hudson.queue.schedule(job)
    
    stage 'Test Script'
    sh 'sh test.sh'
}
