pipeline {
    agent any
     environment ('Set Variable database') {
        dbname="JSONATTACK"
    }
    stages {
        stage('Get Wallet') {
                environment {
                      corret_status="AVAILABLE"
                }
                steps {
                timeout(time: 30, unit: 'SECONDS') {
                        waitUntil {
                            script {
                            def status = """${sh(
                                script: 'echo "AVAILABLE" |grep \'AVAILABLE\''
                                 ,returnStdout:true
                                        )}"""
                            return  (status == "AVAILABLE" );
                            println "stampa status2 : " +   status
                         }
                        }
                }
                script {
                    sh 'touch pippo'
                }
            }
        }
    }
}
