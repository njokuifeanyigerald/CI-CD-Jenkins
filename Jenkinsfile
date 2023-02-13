pipeline{
    agent{
        label "node"
    }
    stages{
        stage("sonar quality status"){
            agent{
                docker {
                    image 'maven'
                }
            }
            steps{
                echo "========executing sonar quality status========"
            }
            post{

                success{
                    echo "========sonar quality status executed successfully========"
                }
                failure{
                    echo "========sonar quality status execution failed========"
                }
            }
        }
    }
    post{
        success{
            echo "========pipeline executed successfully ========"
        }
        failure{
            echo "========pipeline execution failed========"
        }
    }
}