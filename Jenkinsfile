pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        echo "Hi!"
        // a run parameter will add _JOBNAME and _NUMBER as additional environment variables
        //echo "Going to consume: devoptics-build-${RUN_NUMBER}"
        //echo "And going to consume: devoptics-lib-build-${LIB_RUN_ID}"
        //gateConsumesRun jobName: "${RUN_JOBNAME}", runId: "${RUN}"
        //gateConsumesRun jobName: "devoptics-lib-build/master", runId: "${LIB_RUN_ID}"
        //gateConsumesRun jobName: 'cat/devoptics-lib-build/master', masterUrl: 'https://cbcore.gke.kearos.net/teams-cat/', runId: "${LIB_RUN_ID}"

        // deprecated steps as of February 2019
        //devOpticsConsumes file: '', id: "devoptics-build-${RUN_NUMBER}", 
        //  jobName: "${RUN_JOBNAME}",
        //  masterUrl: '', runId: "${RUN}", type: 'demo'
      }
    }
  }
}
