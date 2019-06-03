# CDAAC_COSMIC-TEC_Data-Research

Python codes based on Jupyter Notebook is used to process CDAAC COSMIC netcdf files, for Research on TEC.  
Part of the code explanation is in Chinese, but the code in all is very easy and seperated into parts thanks to the Jupyter feature.


_All podTec and ionPrf files are deleted, please download yourself from [CDAAC](https://cdaac-www.cosmic.ucar.edu/),  
but all file paths are shown in code, files are on 1 April 2011 of COSMIC mission._


### A MAJOR PROBLEM:

 Due to the lack of related knowledge,   
&#8195; the method to __calculate tangent point with the data from podTec file__ is not found.
          
  Therefore all the TEC results from podTec data have no practical meaning,  
 &#8195;_(Due to an uncertainty of location for the TEC mearsuring point)_   
&#8195;only the results from ionPrf are correct.   
&#8195; _(ionPrf is a final product file of CDAAC which contains exact location of one point and its TEC)_  
   
 If you have a way to **calculate tangent point with GPS & LEO location and Elevation Angle,**   
&#8195; I would be more than grateful of your help.


## Requires:
  * Python 3.7
  * CDAAC files (netcdf file including podTec and ionPrf)
  * Python libraries: (   netCDF4
                           numpy
                           math
                           matplotlib
                           basemap      )
                           
                           
## Process:
  * Read data from nc files
  * ECEF-LLA (Longitude, latitude, altitude) transformation
  * GPS/LEO (Low Earth Orbit) projection trajectory plot
  * Batch processing 
  
  
## Output:   
  * Trajectories of LEO/GPS
  * TEC shown as colormap along tangent point trajectory
  * TEC-Altitude figure of data from different trajectories/nc files
