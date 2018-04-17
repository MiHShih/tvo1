AUTOMAG can pick amplitudes for Ml and make spectra used for automatically determining Mw from the spectral level. The program can work from EEV on single events \(described in section 6.7\) or with many events as described here. The default option in EEV is to use only Z and S-phases, however more options are available \(also in EEV, see manual\).

* Select 3 events to use with EEV. Go to 199606 with EEV and select events 2,3 and 6 with EEV command ‘c’. The S-files of the 3 events are now stored in file eev.out.

* Run AUTOMAG. Input file is eev.out. Use all defaults for Spec and wa windows and spectral range.

* For station code and component, select ALL meaning Z-channels will be used.

* For spectrum type, use default \(S\)

The program will now calculate Ml and Mw for all events and at the end there will be a statistics for the average magnitudes of all events. Output of all the automatic determinations is found in automag.out.





Spectra are by default calculated using S-phases. But they can also be calculated using P-phases. In this case one has to make sure that the S-P time is long enough for the spectral window. The default 20 s is often too long for local events and the data will be rejected. The following is a test for using P-phases.

* Run AUTOMAG. Input file is eev.out. Use 10 s for Spec window and 50 s for wa window. Use default for spectral range.

* For station code and component, select ALL meaning Z-channels will be used.

* For spectrum type, use p.



