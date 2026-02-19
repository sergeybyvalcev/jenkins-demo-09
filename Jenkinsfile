pipeline
{
    agent {
        label '1C_agent'
    }

    environment {
        envString = 'world'
    }

    post {
        always {            
           bat "echo always"
        }

        failure {
            bat "echo failure"
        }

        success {
            bat "echo succes"
        }

    }

    stages {
        // stage("First step") {
        //     steps {                
        //         bat "chcp 65001\n echo Hello, ${envString}"
        //     }
        // } 
        stage("Build test base") {
            steps {                
                bat "chcp 65001\n vrunner init-dev --v8version=8.3.23.1912 --dt C:\\jenkins\\template\\dev.dt --db-user Teacher --src C:\\repo\\jenkins-demo-09\\src --ibconnection /FC:\repo\jenkins-demo-09\build\ib"
            }
        }       
        // stage("Syntax check") {
        //     steps {                
        //         bat "chcp 65001\n vrunner syntax-check"
        //     }
        // }
        // stage("Smoke tests") {
        //     steps {
        //         script {
        //             try {
        //                 bat "chcp 65001\n vrunner xunit"
        //             }
        //             catch(Exception Exc) {
        //                 currentBuild.result = 'UNSTABLE'
        //             }
        //         }                
        //     }
        // }
        // stage("Vanessa") {
        //     steps {
        //         script {
        //             try {
        //                 bat "chcp 65001\n vrunner vanessa"
        //             }
        //             catch(Exception Exc) {
        //                 currentBuild.result = 'UNSTABLE'
        //             }
        //         }                
        //     }
        // } 
        // stage("Sonar") {
        //     steps {
        //         script {
        //             scannerHome = tool 'sonar-scanner'
        //         }
        //         withSonarQubeEnv("sonar") {
        //             bat "chcp 65001\n ${scannerHome}/bin/sonar-scanner -D sonar.login=sqp_ff1f8486e5db41bcca28e81970a89395690440a4"
        //         }                
        //     }
        // } 
    }
}