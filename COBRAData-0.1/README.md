# COBRAData

## Introduction
COBRAData module models & structures MRI-related measurements and derived data to custom XNAT data-types (ImageData assessments) for integrating them in XNAT. Derived data-types have been designed and conceived for covering [COBRA project](http://fp7-cobra.eu/) data needs (WP3 Neuro-imaging).

## Installation procedure

1. Get the lattest version of the module as follows: 
  ```
  git clone https://github.com/jhuguetn/xnat-modules.git xnat-modules
  ```

2. Create the module jar file (more info [here](https://wiki.xnat.org/display/XNAT16/Exploring+Module+Structure)): 
  ```
  cd xnat-modules/COBRAData
  jar cf ${modules_location}/COBRAData.jar *
  ```

3. Re-update XNAT webapp (more info [here] (https://wiki.xnat.org/display/XNAT16/Setting+Up+and+Updating+XNAT)):
  ```
  bash ${XNAT_HOME}/bin/update.sh -Ddeploy=true
  psql -h {HOSTNAME} -d {XNAT_DB_NAME} -U {XNAT_DB_USER} -f ${XNAT_HOME}/deployments/xnat/sql/xnat-update.sql 
  ```

## Questions/Comments?

Submit an issue, fork and/or PR. Alternatively, reach me at j.huguet(at)amc.uva.nl

## Credits

This work has been supported by the European Union’s Seventh Framework Programme for research.

