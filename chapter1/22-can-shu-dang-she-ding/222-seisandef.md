SEISAN.DEF lists general parameters used in SEISAN. Note that the parameters must be aligned with the ‘Par 1’ and ‘Par 2’ markers since the file is read by Fortran, which reads a fixed format statement. There are several parameters in SEISAN.DEF that should be modified for use in a particular observatory.



The parameters to be modified are:  
 

WAVEFORM\_BASE: the name of your event database; here, CVE.

CONT\_BASE: the name\(s\) of your continuous database\(s\) to be searched for trace data when starting MULPLT in continuous \(CONT\) mode. In our example, it is CVC.

COPY\_WAVE DIR: the name of your event database, for use when registering events. Again here, CVE

MERGE\_WAVEFORM: the 2-character network ID used to name the waveforms when registering. Here, CC.

CONT\_BEFORE: when using MULPLT in CONT mode, the number of minutes of waveform data to be read into memory before the required start time. CONT\_BEFORE must be at least as long as the waveform file. Here, 10.

CONT\_AFTER: when using MULPLT in CONT mode, the number of minutes of waveform data to be read into memory after the data that is plotted. Here, 10.

MAP\_LAT\_BORDER: , MAP\_LON\_BORDER: Used with MAP in EEV, which plots a map around the current epicenter. These 2 parameters give the distance in degrees from the epicenter to the edges of the map

EPIMAP\_STATIONS: Indicator for EPIMAP to plot stations, ‘A’ will plot the stations. EPIMAP\_MAP\_FILE: the names of the maps to use with MAP option in EEV.



