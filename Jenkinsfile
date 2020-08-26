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
                    echo bat(returnStdout: true, script: 'cd C:\\jenkins\\workspace\\python_test\\Python3 && py -3 Hello_python3.py')
                    
                    
                }
            }
        }
    }
}
