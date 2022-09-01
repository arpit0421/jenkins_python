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
        stage("configure Python"){
            steps{
                sh "sudo yum install python3 -y"
                sh "sudo yum install python3-pip -y"
                sh "sudo yum install psutil -y"
            }
        }
        stage("run script"){
            steps{
                sh "python3 main.py ${option}"
            }
        }
    }
}