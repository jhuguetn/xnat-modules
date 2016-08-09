#QAPdata

[Quality Assessment Protocol](http://preprocessed-connectomes-project.org/quality-assessment-protocol/)

QAP is a Python-based package for computing functional and anatomical MRI data quality measures. 
QAPdata module structures and models QAP output measurements to inner XNAT datatypes (ImageData assessments) for integrating them as an additional extension to XNAT.

More information about the QAP computed metrics/measurements can be found [here] (http://preprocessed-connectomes-project.org/quality-assessment-protocol/#taxonomy-of-qa-measures).

##Installation procedure:

1. Get the lattest version of the module as follows: 
  ```
  git clone https://github.com/jhuguetn/xnat-modules.git xnat-modules
  ```

2. Create the module jar file (more info [here](https://wiki.xnat.org/display/XNAT16/Exploring+Module+Structure)): 
  ```
  cd xnat-modules/QAPdata
  jar cf ${modules_location}/QAPdata.jar *
  ```

3. Re-update XNAT webapp (more info [here] (https://wiki.xnat.org/display/XNAT16/Setting+Up+and+Updating+XNAT)):
  ```
  bash ${XNAT_HOME}/bin/update.sh -Ddeploy=true
  psql -f ${XNAT_HOME}/deployments/xnat/sql/xnat-update.sql
  ```

##Questions/Comments?

Submit an issue, fork and/or PR. Alternatively, reach me at j.huguet(at)amc.uva.nl
