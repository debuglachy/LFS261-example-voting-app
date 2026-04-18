pipeline {
    agent any 

    tools{
		maven 'maven 3.9.8'

    }

    stages{
        stage("build"){
            steps{
                echo 'Compiling worker app'
                dir('worker'){
			sh 'mvn compile'
		}
            }
        }
        stage("test"){
            steps{
                echo 'Entering test stage'
                
            }
        }
        stage("package"){
            steps{
                echo 'Packaging worker app'

            }
        }
    } 

    post{
      always{
          echo 'Building multi-branch pipeline is completed.'
      }
    }
}
