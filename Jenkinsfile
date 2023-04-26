
def gv

pipeline {
  agent any
    stages{
          stage("init")
          {
            steps{
                script{
                
                gv=load "nara.groovy"

            }
            }

            
          }

      stage("build")
        {

          steps{
                script{
            gv.build()
            
          }

          }

        }



  }
  }
