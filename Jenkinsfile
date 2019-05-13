pipeline{
    agent{
        docker {
            image 'node:9-alpine'
            args '-p 3000:3000'
        }
    }
    stages{
        stage("Build"){
            steps{
                sh 'npm install'
            }
            post{
                always{
                    echo "Done the build stage"
                }
                success{
                    echo "Build: Success"
                }
                failure{
                    echo "Build: Failure"
                }
            }
        }
    }
    post{
        always{
            echo "All done"
        }
        success{
            echo "All: Success"
        }
        failure{
            echo "All: Failure"
        }
    }
}