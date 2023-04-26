
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
          input{
            message "select as the env ron"
            ok "done"
          }
          parameters{
            choice(name:"env",choices:["dev","stg","prod"])

          }
          steps{
                script{
            gv.build()
            echo "deploying to ${env}"
          }

          }

        }



  }
  }
