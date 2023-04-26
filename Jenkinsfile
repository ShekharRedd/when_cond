
pipeline {
  agent any
  parameters{
    choice(name:'VERSION',choices:['a.py','b.py','c.py'],description:'')
    booleanParam(name:'exeuteTests',defaultValue:true,description:'')

  }
    stages{
      stage("build")
        {
          when{
            expression{
              params.exeuteTests
            }
          }
          steps 
            { 
              echo "hello world"
            }
        }
      stage("deplov")
        { 
          steps
              { 
                echo "deploy successfully"
              }

        }
      stage("python files execute"){
        // when{
        //   expression{
        //     params.pythonfiles
        //   }
        // }
        steps{
          sh "python ${VERSION}"
        }
        steps{
          echo "hello worlssdfs df"
        }

  }

    }

  }
