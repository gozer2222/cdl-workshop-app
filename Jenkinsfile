
   stage('build & unit tests'){
        node('build'){
            sh 'sleep 10s;'
        }
   }
   stage('integration tests'){
        node('build'){
            sh 'sleep 20s;'
        }
   }
   stage('acceptance-tests'){
        node('build'){
            sh 'sleep 10s;'
            parallel (
                chrome: { sh "sleep 10s;" },
                edge: { sh "sleep 10s;" },
                firefox: { sh "sleep 10s;" }
            )
        }
   }
   stage('staging'){
        node('ssh'){
            sh 'sleep 10s;'
        }
   }
   stage('manual-approval'){
       input "GO prod ?"
   }
   stage('deploy'){
        node('ssh'){
            sh 'sleep 10s;'
        }
   }
