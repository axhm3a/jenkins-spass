node {
  for (int i=0; i< 2; ++i) {  
    stage "Stage #"+i
    print 'Hello, world $i!'
  }

  stage "Stage Parallel"
  def branches = [:]
  for (int i = 0; i < 5; i++) {
    branches["split${i}"] = {
       echo  'Starting sleep'
       sleep 10
       echo  'Finished sleep'
    }
  }
  parallel branches
}
