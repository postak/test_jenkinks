pipeline {
    agent any 
     environment ('Set Variable database') {
        // variabili per identificare l'autonomous  
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
                                            ,returnStatus:true 
                                        )}""" 
                            return  (status == "AVAILABLE" );  
                            println "stampa status : " +   status 
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
