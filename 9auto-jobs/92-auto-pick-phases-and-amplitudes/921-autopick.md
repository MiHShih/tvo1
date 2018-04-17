The program AUTOPICK can pick phases for one or several events already registered in a data base. The program is either operated in EEV for one event using command ‘z’, or several events are processed using program AUTO. An example parameter file is already set up in DAT. In AUTOPICK all channels to be used must be defined in the parameter file so the program can be tailored to specific stations.

* Select event 19960705

* Delete already picked phases using the editor or the EEV command dels, make sure to keep all header lines.

* Give command ‘z’ and phases should be picked and saved in S-file.

* Plot event and inspect automatic picks, note that all picks are marked as E for emergent.

* Locate event



training dataset in SEISAN

The Portuguese network has long used AUTOPIC and therefore have well adjusted parameters. The following event \(courtesy Fernando Carrilho\) is from the Azores network. The data is located in WOR/azores. The data include AUTOPICK.DEF, station file and calibration files so it can also be used for testing magnitudes. There is one event without readings.

* Go to WOR/azores

* Type eev

* Type z and get the automatic readings

* Check the picks by plotting

* Locate with and without rejecting bad phases

* For the good phases also run command am to get automatic magnitudes

* Compare magnitudes and location to the official location in S-file





