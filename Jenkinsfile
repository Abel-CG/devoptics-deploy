pipeline {
  agent any
  parameters {
    run description: 'Run for Build', filter: 'SUCCESSFUL', name: 'RUN', projectName: 'devoptics/demomon/devoptics-build/master'
    run description: 'Run for Build Lib', filter: 'SUCCESSFUL', name: 'RUNLIB', projectName: 'https://cbcore.gke.kearos.net/teams-cat/job/cat/job/devoptics-lib-build/job/master/'
  }
  stages {
    stage('Build') {
      steps {
        // a run parameter will add _JOBNAME and _NUMBER as additional environment variables
        echo "Going to consume: devoptics-build-${RUN_NUMBER}"
        echo "And going to consume: devoptics-lib-build-${RUNLIB_NUMBER}"
        gateConsumesRun jobName: "${RUN_JOBNAME}", runId: "${RUN}"
        gateConsumesRun jobName: "${RUNLIB_JOBNAME}", masterUrl: 'https://cbcore.gke.kearos.net/teams-cat/', runId: "${RUNLIB}"

        // deprecated steps as of February 2019
        //devOpticsConsumes file: '', id: "devoptics-build-${RUN_NUMBER}", 
        //  jobName: "${RUN_JOBNAME}",
        //  masterUrl: '', runId: "${RUN}", type: 'demo'
      }
    }
  }
}
