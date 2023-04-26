
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
          steps{
                script{
            gv.build()
           
            
          }
          }

        }

  }
  }
