
node {
    stage('Clone sources') {
        git url: 'https://github.com/Mugundhanp2497/pipe-ine.git'
    }
    stage('Gradle build') {
          echo "king"
    }

    stage('Publish build info') {

    echo "queen" 
    }
    stage("Parallel") {
  steps {
    parallel (
      "Taskone" : {
        do some stuff
      },
      "Tasktwo" : {
         Do some other stuff in parallel
      }
    )
  }
}
}
    
