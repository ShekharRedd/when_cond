
def gv

pipeline {
  agent any
  parameters{
    choice(name:"pythonfiles",choices:['a.py','b.py','c.py'])
    booleanParam(name:'exeuteTests',defaultValue:true,description:'')
    
  }
    stages{
          stage("init"){
            gv=load "nara.groovy"
          }

      stage("build")
        {
          when{
            expression{
              params.exeuteTests
            }
          }
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
        // when{
        //   expression{
        //     params.pythonfiles
        //   }
        // }
        script{
          gv.envn()
        }

      }
  }


  }
