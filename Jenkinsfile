    node {

    stage('Clone From Git') {
    def command = "git pull origin pull/$CHANGE_ID/head"
    def proc = command.execute()
    proc.waitFor()              

    println "Process exit code: ${proc.exitValue()}"
    println "Std Err: ${proc.err.text}"
    println "Std Out: ${proc.in.text}" 
    }
    
    stage('Test Script') {
    sh 'sh test.sh'
    }
    }
