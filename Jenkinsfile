node {

    stage('Clone From Git') {
    def command = "git --version"
    def proc = command.execute()
    proc.waitFor()              

    println "Process exit code: ${proc.exitValue()}"
    println "Std Err: ${proc.err.text}"
    println "Std Out: ${proc.in.text}" 
    }
    stage('test') {            
    println "Std Out: ${env.CHANGE_ID}" 
    }
    
    stage('Test Script') {
    sh 'sh test.sh'
    }
}
