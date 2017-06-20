This exercise aims to use netCDF-4 vlen type to replace the CF ragged array representation of data variables in an argo netCDF file. The varied dimension(fastest changing dimension) in this case is N_LEVEL. In the vlen netCDF file, the N_LEVEL is gone. The CDL headers of the original netCDF-3 Argo file and the vlen netCDF-4 Arog file are listed under this directory.

   vlen type file: 20160901_prof_vlen.nc4.hdr

   original file: 20160901_prof.nc.hdr


The original netCDF-3 file and the corresponding vlen netCDF-4 file can be found under a ftp server described below. 


   I downloaded the original netCDF file from the argo-float data ftp site 
   under ftp://usgodae.org/pub/outgoing/argo/latest_data/
   Since they frequently update their latest_data directory, I put a copy of the example file under
   ftp://gamma.hdfgroup.org/pub/outgoing/ymuqun/earth-cube/DSG/argo-float/vlen/20160901_prof.nc

   The final netCDF-4 file with vlen can be found under 
   ftp://gamma.hdfgroup.org/pub/outgoing/ymuqun/earth-cube/DSG/argo-float/vlen/20160901_prof_vlen.nc4

The following explains the steps to use NCO to prepare the vlen type netCDF file.

1. Generate a netCDF-4 extended model file.
   nccopy -k'netCDF-4' -d 2 -s 20160901_prof.nc 20160901_prof.nc4
2.
From the nc4 file, first generate a nc file by extracting the variables that can be represented by vlen and the varied dimension is N_LEVEL. These variables are: "CNDC,CNDC_ADJUSTED,CNDC_ADJUSTED_ERROR,CNDC_ADJUSTED_QC,CNDC_QC,PRES,PRES_ADJUSTED,PRES_ADJUSTED_ERROR,PRES_ADJUSTED_QC,PRES_QC,PSAL,PSAL_ADJUSTED,PSAL_ADJUSTED_ERROR,PSAL_ADJUSTED_QC,PSAL_QC"

ncks -x -v TEMP,TEMP_ADJUSTED,TEMP_ADJUSTED_ERROR 20160901_prof.nc4 20160901_prof_noTEMP.nc4
ncks -x -v  CNDC,CNDC_ADJUSTED,CNDC_ADJUSTED_ERROR,CNDC_ADJUSTED_QC,CNDC_QC,PRES,PRES_ADJUSTED,PRES_ADJUSTED_ERROR,PRES_ADJUSTED_QC,PRES_QC,PSAL,PSAL_ADJUSTED,PSAL_ADJUSTED_ERROR,PSAL_ADJUSTED_QC,PSAL_QC 20160901_prof_noTEMP.nc4 20160901_prof_noALL.nc4

3. The extracted variables above then are added to 20160901_prof_noALL.nc4 with vlen datatype. The final file with veln type is 20160901_prof_vlen.nc4

