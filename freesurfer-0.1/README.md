# FreeSurfer

## Introduction
[FreeSurfer](https://surfer.nmr.mgh.harvard.edu) is an open source software suite for processing and analyzing (human) brain MRI images. 

FreeSurfer module shapes FreeSurfer output stats metrics as custom XNAT data-types (ImageData assessments) for integrating them as an additional information type to XNAT.

### Taxonomy of FreeSurfer output metrics 
* Subcortical segmentation (asec.stats), more info [here](http://surfer.nmr.mgh.harvard.edu/fswiki/FsTutorial/VolumetricGroupAnalysis#aseg.stats)
* Cortical parcellation (lh.aparc.stats & rh.aparc.stats), more info [here](http://surfer.nmr.mgh.harvard.edu/fswiki/FsTutorial/VolumetricGroupAnalysis#aparc.stats)

## Installation procedure

1. Get the lattest version of the module as follows: 
  ```
  git clone https://github.com/jhuguetn/xnat-modules.git xnat-modules
  ```

2. Create the module jar file (more info [here](https://wiki.xnat.org/display/XNAT16/Exploring+Module+Structure)): 
  ```
  cd xnat-modules/freesurfer
  jar cf ${modules_location}/freesurfer.jar *
  ```

3. Re-update XNAT webapp (more info [here] (https://wiki.xnat.org/display/XNAT16/Setting+Up+and+Updating+XNAT)):
  ```
  bash ${XNAT_HOME}/bin/update.sh -Ddeploy=true
  psql -f ${XNAT_HOME}/deployments/xnat/sql/xnat-update.sql
  ```

## Questions/Comments?

Submit an issue, fork and/or PR. Alternatively, reach me at j.huguet(at)amc.uva.nl
