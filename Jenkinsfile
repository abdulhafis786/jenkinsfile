pipeline {
    
    agent any
	parameters {
		choice(name: 'VERSION', choices:['1.1.0','1.2.0','1.3.0'], description: '')
                booleanParam(name: 'executetests', defaultValue: true, description:'')

    stages {
        
        stage("build") {
           
           steps {

                echo "Trying to build..."
          }
       }

         stage("Test") {
		 when { 
                     expression {
                    params.executetests
		}
           }           
           steps {

                echo "Trying to test..."
          }
       }
	
          stage("deploy") {
           
           steps {
                echo "Trying to deploy..."
		echo "deploying version ${params.VERSION}"
          }
       }

    }

}
