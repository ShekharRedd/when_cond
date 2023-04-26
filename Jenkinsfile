
def gv

pipeline {
  agent any
    stages{
          stage("init")
          {
            steps{
                script{
                
                gv=load "nara.groovy"
                gv.build()
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
