pipeline {
    agent {label 'windows'}
    stages {
        stage('build') {
            steps {
                script {
                    //echo "**************Show env variables *******************"
                    //echo env.PATH
                    //bat 'echo %PATH%'
                    //bat 'wmic computersystem get name'
                    //echo bat(returnStdout: true, script: 'dir')
                    //echo "**************Show Chocolatey help *******************"
                    //echo bat(returnStdout: true, script: 'choco -?')
                    //echo "**************Install python *******************"
                    //echo bat(returnStdout: true, script: 'choco install python -y')
                    echo "************** Run python v3 file *******************"
                    echo bat(returnStdout: true, script: 'cd C:\\jenkins\\workspace\\python_test\\Python3 && py -3 Hello_python3.py')
                    
                    
                }
            }
        }
    }
    post {
        
        success {
            echo 'Next steps Creating a pip requeriments file, creating new scripts in python 2 and 3, using test on python venvs '
            options {

                buildDiscarder(
                    logRotator(
                        // number of build logs to keep
                        numToKeepStr:'5',
                        // history to keep in days
                        daysToKeepStr: '15',
                        // artifacts are kept for days
                        artifactDaysToKeepStr: '15',
                        // number of builds have their artifacts kept
                        artifactNumToKeepStr: '5'
                    )
                )
            }
        }
        failure {
            echo 'This will run only if failed'
        }
        unstable {
            echo 'This will run only if the run was marked as unstable'
        }
        changed {
            echo 'This will run only if the state of the Pipeline has changed'
            echo 'For example, if the Pipeline was previously failing but is now successful'
        }
    }
}
