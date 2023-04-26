
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

        stage("bui")
        {

          input{
                message "hello world"
                ok "Done"

          
          parameters{
              choice(name:"env",choices:["dev","enc"])
          }
          
          }
          steps{
                script{
            gv.build()
               echo "env employ ${env}"
            
          }
          }

        }

  }
  }
