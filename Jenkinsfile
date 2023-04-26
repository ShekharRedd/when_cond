
def gv

pipeline {
  agent any
  parameters{
    choice(name:"pythonfiles",choices:['a.py','b.py','c.py'])
    booleanParam(name:'exeuteTests',defaultValue:true,description:'')
    
  }

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
            echo "hello ${env}"
            
          }

          }

        }



  }
  }
