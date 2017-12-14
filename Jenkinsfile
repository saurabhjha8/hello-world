
checkpoint "checkpoint before node master"
node {
    echo "Build ID: env.BUILD_ID"
}

checkpoint "checkpoint before default node"
node {
    
     properties([
  	       parameters([
  		       string(name: 'VALUE1', defaultValue: '1', description: 'Provide value1'),
               string(name: 'VALUE2', defaultValue: '2', description: 'Provide value2')
  	                 ])
               ])  
  echo "VALUE1 = ${VALUE1}"
  echo "VALUE2 = ${VALUE2}"
    echo "Build Number: env.BUILD_NUMBER"
    
    script {
     if (VALUE1 != VALUE2) {
            echo 'Values are not equal'
            sh "exit 1"
            currentBuild.result = 'FAILURE'
            
        } 
    }
    
     stage('Build') {
   echo 'Hello Build'
     }
    
      stage('Deploy') {
          echo 'Hello Deploy'
      }
}


