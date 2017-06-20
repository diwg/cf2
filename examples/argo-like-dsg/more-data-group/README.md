This exercise aims to see if we can use netCDF-4 groups to reasonably combine several Argo netCDF files into an argo netCDF file. 
The latest argo-float data can be found under ftp://usgodae.org/pub/outgoing/argo/latest_data/
Under that directory, you may find that the observational data under each day are stored in several netCDF files. For example, on Oct.27th, 2016(20161027),
you may find netCDF-3 files R20161027_prof_0.nc, R20161027_prof_1.nc,..... R20161027_prof_8.nc. 

According to the Argo-float user manual(can be found under http://www.argodatamgt.org), These files share some common variables and attributes,so one can use one netCDF-4 file to combine all these files into one file. The shared variables and attributes can be put under the root group and all the other objects will be put under different sub-groups. 

 The CDL headers of one original netCDF-3 Argo file and the netCDF-4 Arog file that uses groups to combine all the netCDF-files are listed under this directory.

   The first original file: R20161027_prof_0.nc.hdr
   The combined file: R20161027_prof_all.nc.hdr 


The original netCDF-3 file and the corresponding vlen netCDF-4 file can be found under a ftp server described below. 

   I downloaded the original netCDF file from the argo-float data ftp site 
   under ftp://usgodae.org/pub/outgoing/argo/latest_data/
   Since they frequently update their latest_data directory, I put all the original example files under
   ftp://gamma.hdfgroup.org/pub/outgoing/ymuqun/earth-cube/DSG/argo-float/cf-groups/orig-files/20161027/


   The final combined netCDF-4 file can be found under 
   ftp://gamma.hdfgroup.org/pub/outgoing/ymuqun/earth-cube/DSG/argo-float/cf-groups/R20161027_prof_all.nc

