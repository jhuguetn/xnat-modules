# xnat-modules
XNAT modules repository:
* QAPdata

```
git clone https://github.com/jhuguetn/xnat-modules.git
cd xnat-modules/QAPdata
jar cf ${modules_location}/QAPdata.jar *
cd /xnat/xnat_builder #or whatever location XNAT sources are in
bin/update.sh -Ddeploy=true 2>&1
cd deployments/xnat
psql -f sql/xnat-update.sql
```
