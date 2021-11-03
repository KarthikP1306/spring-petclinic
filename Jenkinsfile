pipeline{
    agent none
    stages{
        stage("Maven Install"){
            agent{
                docker{
                    image 'maven:3.5.0'
                }
            }

            steps{
                echo "========executing mvn install========"
                sh 'mvn clean install'
            }
            // post{
            //     always{
            //         echo "========always========"
            //     }
            //     success{
            //         echo "========A executed successfully========"
            //     }
            //     failure{
            //         echo "========A execution failed========"
            //     }
            // }
        }
        // stage('Docker Build'){
            
        // }
    }
    post{
        always{
            echo "========always========"
        }
        success{
            echo "========pipeline executed successfully ========"
        }
        failure{
            echo "========pipeline execution failed========"
        }
    }
}
