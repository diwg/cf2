This is the first example to use the group to store the argo-like profile/trajectory case. The argo-float data files I examine can be found under ftp://usgodae.org/pub/outgoing/argo/dac/bodc/1900083/profiles/
I here just create a much simpler example to show how one can use group to organize many files into one file and how CF-2 may just enforce the inheritenance of attributes from the parent group to the children groups.

group_cf_traj_prof.cdl is essentially the combination of cf_traj_prof1.cdl and cf_traj_prof2.cdl
The common information shared by the two files is moved to the root group.
