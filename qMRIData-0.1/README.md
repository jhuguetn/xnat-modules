# qMRIData

## Introduction
The qMRIData module captures the Quantitative MRI processing pipeline output measurements generated into custom XNAT data-types (ImageData assessments).

More information about the Quantitative MRI processing pipeline guts can be found [here] (https://github.com/jhuguetn/xnat-pipelines/tree/master/qMRI).

## Installation procedure

1. Get the lattest version of the module as follows: 
  ```
  git clone https://github.com/jhuguetn/xnat-modules.git xnat-modules
  ```

2. Create the module jar file (more info [here](https://wiki.xnat.org/display/XNAT16/Exploring+Module+Structure)): 
  ```
  cd xnat-modules/qMRIData
  jar cf ${modules_location}/qMRIData.jar *
  ```

3. Re-update XNAT webapp (more info [here] (https://wiki.xnat.org/display/XNAT16/Setting+Up+and+Updating+XNAT)):
  ```
  bash ${XNAT_HOME}/bin/update.sh -Ddeploy=true
  psql -h {HOSTNAME} -d {XNAT_DB_NAME} -U {XNAT_DB_USER} -f ${XNAT_HOME}/deployments/xnat/sql/xnat-update.sql 
  ```

## Questions/Comments?

Submit an issue, fork and/or PR. Alternatively, reach me at j.huguet(at)amc.uva.nl
