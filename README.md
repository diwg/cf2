# CF2

There are multiple efforts to extend the Climate-Forecast (CF) metadata convention.
The National Science Foundation (NSF) supports the EarthCube "Advancing netCDF-CF for the Geoscience Community" [project](https://github.com/Unidata/EC-netCDF-CF) that organizes some of these efforts.
Project members have gathered scientific use-cases and example datasets (including [these](https://github.com/diwg/diwg)) to guide the drafting of enhancements to the CF standard.
Since some proposed enhancements break backwards compatibility with CF, this effort is loosely known as "CF2", although no formal relation between CF2 and CF yet exists.

Notable proposed extensions include:
- [Encoding of Swath Data in the Climate and Forecast Convention](https://github.com/Unidata/EC-netCDF-CF/blob/master/swath/swath.adoc).
- [CF2-Group: Draft Extension for Files with Groups](https://github.com/diwg/cf2/blob/master/group/cf2-group.adoc).
- [Use of netCDF-4 data types in CF-2 files](https://github.com/diwg/cf2/blob/master/types/new-types.adoc)

The Swath proposal allows for features described in the Group proposal, though it can be implemented without those features.
Both the Swath and the Group proposals were endorsed/approved (in close to their current form) by participants at the 2017 CF2 Workshop in Boulder, and, more recently by NASA's Dataset Interoperability Working Group (DIWG) in 2018. 
We welcome new efforts and contributions to ongoing efforts that improve dataset interoperability.

# CF2-Group

## Current Draft

[CF2-Group: Draft Extension for Files with Groups](https://github.com/diwg/cf2/blob/master/group/cf2-group.adoc)

The Group proposal is compatible with most existing NASA and ESA satellite datasets. NCO 4.7.4 contains a working implementation of the algorithms to locate Out-of-Group (OOG) identifiers, and may be used to vet datasets designed to comply with CF2-Group. 

## Previous Work

Earlier discussions and proposal drafts for utilizing Groups in CF2 are still viewable for their historical provenance.
These efforts were conducted as part of NASA Dataset Interoperability Working Group (DIWG) and date back to 2013:

Original [proposal](http://mailman.cgd.ucar.edu/pipermail/cf-metadata/2013/056827.html) to CF list, September 15, 2013

This effort migrated to the EarthCube project from 2015-2018, when the CF2-Group draft proposal was collaboratively shared:

Google doc [proposal](https://docs.google.com/document/d/1KK6IZ2ZmpaUTVgrw-GlFd6almppjvGz6D7nxVTO3BtI/edit)

# CF2 and Discrete Sampling Geometries (DSG)

Some notes on CF extensions for Discrete Sampling Geometries (DSG) are archived below.

201605 DSG [notes](https://docs.google.com/document/d/1onf6yJAF6h2_idaQJWKcBPcaHE9WRs4ZUcbidZflgZI/edit)

201609 DSG [report](https://docs.google.com/document/d/1Hfgw-jDuJrmsmHXRsUxjrrzuyA8tWwosZTIC-byryGU/edit)
