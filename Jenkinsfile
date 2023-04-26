
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
            script{
                gv=load "nara.groovy"
            }
            
          }

      stage("build")
        {
          script{
            gv.build()
          }
        }
      stage("deplov")
        { 
          script{
            gv.deploy()
            }
        }
      stage("python files execute"){

        script{
          gv.envn()
        }

      }
  }
  }
