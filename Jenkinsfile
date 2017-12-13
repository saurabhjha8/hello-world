checkpoint "checkpoint before node"
node {
    
     properties([
  	       parameters([
  		       string(name: 'VALUE1', defaultValue: '1')
  	                 ])
               ])  
  echo "VALUE1 = ${VALUE1}"
    
    
    checkpoint "checkpoint before stage Dev"
     stage('Build') {
   echo 'Hello Build'
     }
    
     checkpoint "checkpoint before stage Deploy"
      stage('Deploy') {
          echo 'Hello Deploy'
      }
}
