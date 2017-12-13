checkpoint "checkpoint before node"
node {
    
     properties([
  	       parameters([
  		       string(name: 'VALUE1', defaultValue: '1', description: 'Provide value1'),
               string(name: 'VALUE2', defaultValue: '2', description: 'Provide value2')
  	                 ])
               ])  
  echo "VALUE1 = ${VALUE1}"
  echo "VALUE2 = ${VALUE2}"
    
     if (${VALUE1} != ${VALUE2}) {
            echo 'Values are not equal'
        } 
    
    checkpoint "checkpoint before stage Dev"
     stage('Build') {
   echo 'Hello Build'
     }
    
     checkpoint "checkpoint before stage Deploy"
      stage('Deploy') {
          echo 'Hello Deploy'
      }
}
