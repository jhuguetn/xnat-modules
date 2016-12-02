#Resources display

##Introduction
The 'resources_display' module is actually a tiny hack that includes an additional Display Field in data-type listings with an aggregate of existing resource collections per each session, similar to and inspired by the existing mrSessionsData 'Scans' field. The hack was initially conceived for easing data validation/analysis at the [COBRA project](http://fp7-cobra.eu/) (WP3 Neuro-imaging).

The module is mainly composed by a set of attributed gathered in an display XML file, the most rellevant of which is the SQLView element which contains an SQL query to gather the aggregate of existing resource collections to be displayed as an additional data-type listing column. 

This module eases end-user checks for existing resource collections as they may be listed, filtered by and/or exported (CSV). For now solely MRSessions data-type display document is affected. In a future might be extended to others (i.e. subjectData, other experiments,... ).

Note that installing this XNAT module implies slightly modifying the database, i.e. creating additional database views. 
More information & documentation about Display Documents can be found [here](https://wiki.xnat.org/display/XNAT16/XNAT+Display+Documents).

##Installation procedure

1. Get the lattest version of the module as follows: 
  ```
  git clone https://github.com/jhuguetn/xnat-modules.git xnat-modules
  ```

2. Create the module jar file (more info [here](https://wiki.xnat.org/display/XNAT16/Exploring+Module+Structure)): 
  ```
  cd xnat-modules/resources_display
  jar cf ${modules_location}/resources_display.jar *
  ```

3. Re-update XNAT webapp (more info [here] (https://wiki.xnat.org/display/XNAT16/Setting+Up+and+Updating+XNAT)):
  ```
  bash ${XNAT_HOME}/bin/update.sh -Ddeploy=true
  psql -h {HOSTNAME} -d {XNAT_DB_NAME} -U {XNAT_DB_USER} -f ${XNAT_HOME}/deployments/xnat/sql/xnat-update.sql 
  ```

##Questions/Comments?

Submit an issue, fork and/or PR. Alternatively, reach me at j.huguet(at)amc.uva.nl

##Credits

This work has been supported by the European Union’s Seventh Framework Programme for research.