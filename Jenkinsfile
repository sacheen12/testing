node {

    stage 'Clone From Git'
    def command = "git --version"
    def proc = command.execute()
    proc.waitFor()              

    println "Process exit code: ${proc.exitValue()}"
    println "Std Err: ${proc.err.text}"
    println "Std Out: ${proc.in.text}" 
    
    stage 'test'
    sh 'echo "ghprbActualCommit: " $ghprbActualCommit'
    sh 'echo "ghprbActualCommitAuthor: " $ghprbActualCommitAuthor'
    sh 'echo "ghprbActualCommitAuthorEmail: " $ghprbActualCommitAuthorEmail'
    sh 'echo "ghprbPullDescription: " $ghprbPullDescription'
    sh 'echo "ghprbPullId: " $ghprbPullId'
    sh 'echo "ghprbPullLink: " $ghprbPullLink'
    sh 'echo "ghprbPullTitle: " $ghprbPullTitle'
    sh 'echo "ghprbSourceBranch: " $ghprbSourceBranch'
    sh 'echo "ghprbTargetBranch: " $ghprbTargetBranch'
    sh 'echo "sha1: " $sha1
    
    stage 'Test Script'
    sh 'sh test.sh'
}
