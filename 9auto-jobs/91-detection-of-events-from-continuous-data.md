The program CONDET can be used to detect events in one or more continuous databases, either a SEISAN continous data base or an archive \(SeisComp or BUD types\). It supports three detection algorithms: 1\) a standard square STA/LTA, 2\) the algorithm suggested by Carl Johnson \([http://www.isti2.com/ew/ovr/carltrig\_ovr.html\](http://www.isti2.com/ew/ovr/carltrig_ovr.html\)\), and 3\) a cross-correlation detector \(which will not be used here\). CONDET can do two things, first to search for triggers on each specified station, and second search for a number of triggers from a given number of stations in a time window \(this requires the first step has been done\).



## Using an archive continuous data base

The archive data base \(SeisComp or BUD\) is in directory archive in WOR so work must be done in WOR. The archive consist of 1 day of LP data from the Danish network. This exercise follow the same steps as the previous ones so you can do the same checks, for details see previous exercise. The main difference is that the data is long period to so trigger parameters are different. ...

* Go to WOR/TVO

* Copy parameter file condet.par from DAT to WOR/TVO. Start by checking the CONDET input file ‘condet.par’, use SEISAN manual for explanation. Parameters to change in the exercise are the detection algorithm, the respective detection parameters, the filters and the network detection settings.

* Now run the program by typing ‘condet’, it automatically uses condet.par as input file. The program runs one station after the other. The main output files are ‘condet.out’ listing all the trigger times, ‘extract.batch’ – a script file to extract the data using the program WAVETOOL, and ‘condet.trace’ which lists the data intervals that were read. Check all these files.



