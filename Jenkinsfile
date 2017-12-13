checkpoint "checkpoint before node"
node {
    
    parameters
  {
    string(name: 'VALUE1', defaultValue: '1', description: 'Pass value1')
    string(name: 'VALUE2', defaultValue: '1', description: 'Pass value2')
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
