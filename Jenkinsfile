pipeline{
    agent any

    parameters {
        string description: 'Enter option to check usage C = CPU, D = Disk, R = RAM', name: 'option'
    }

    stages{
        stage("Build"){
            steps{
                echo "building pipeline"
                echo "usage for ${option}"
            }
        }
        stage("run script"){
            steps{
                sh "python3 main.py ${option}"
            }
        }
    }
}