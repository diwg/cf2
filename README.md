# CF2
Enhancing Climate-Forecast (CF) Conventions with Group Hierarchies

## Previous Work

Some pertinent discussions:

http://mailman.cgd.ucar.edu/pipermail/cf-metadata/2013/056827.html

https://docs.google.com/document/d/1onf6yJAF6h2_idaQJWKcBPcaHE9WRs4ZUcbidZflgZI/edit

https://docs.google.com/document/d/1Hfgw-jDuJrmsmHXRsUxjrrzuyA8tWwosZTIC-byryGU/edit

# CF2 and Discrete Sampling Geometries

### Report from CF2.0+ Workshop
#### Goal:
- Identify which aspects of the enhanced data model would be most beneficial for DSG data
- Develop some concrete steps for implementation of those aspects in CF2.0


#### Discussed the following use cases:
- Argo floats - A ship drops a float which drifts with currents and measures parameters at various depths. Folks might request by buoy number, time slice, spatial coordinates
- Swath - NCEI has swath template, but there isn’t a standard feature type for swaths.
- Time aggregate CTD casts, serve with THREDDS with netCDF subsetting service
- Sensor measures at high frequency (burst or event data), summarized/event data computed for users (see below)

#### Possibilities available via netCDF enhanced model
- Groups, e.g., make a different group for each sample location with a uniquely sized temperature dimension in each group
- VLEN (variable length arrays), e.g., make a vlen temperature dimension

#### DAP discussion and some questions/conclusions:
- Should CF be involved in specifying a **query and delivery system?**
DSG files can be accessed via cdmremote
- what about more generic  simple flat, tables based (SQL-like) query API regardless of underlying data structure.  
- Declarative language - specify what you want, not how to do it. It could greatly simplify requesting subsets of data from a wide variety of underlying data structures.

#### Action items:
- Unidata and others to prototype access of a representational datasets
  - Represent it using groups and VLEN to benchmark access and use performance


- Charlie and others to prototype using groups for metadata for ARGO floats
  - Document what would it take to make that file CF2.0 compliant
  - How does this file become discoverable?  (ie, group data have to repeated?)
  - Does the enhanced metadata actually improve workflow?


- There is a need for tools and conventions that help the community of spreadsheet-using scientists to become part of our CF community.  
    - A set of simple conventions describing how column headers (including units) are specified
    - A set of simple conventions describing how global attributes can be represented in a CSV header
    - Tools that bi-directionally convert between CSV and netCDF-CF DSG (with no information loss) can easily be built.
    - Some candidate tools already exist:  Rosetta, and Panoply
