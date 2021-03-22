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
                            def status = sh(
                                script: 'echo "AVAILABLE" |grep AVAILABLE' ,
                                returnStatus:true
                            )
                            println "stampa status : " +   status
                            return  (status == 0 )
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
