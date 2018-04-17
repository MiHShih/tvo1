

MULPLT permits the use of a single 3-comp station for event location. \(For this capability to be implemented, the RESET TEST\(56\) variable in STATION0.HYP must be set =1, the default setting\) In this technique, the p-arrival, s-arrival and back-azimuth are used to give a general location. The azimuth reading calculated by MULPLT is from the station back to the hypocenter, with reference to True North \(not Magnetic North; note that many 3-comp sensors are oriented with respect to magnetic north. The local magnetic declination must be taken into account to get the true azimuth.\)

Routine processing in Seisan for BPPTK; event location

1. select the p arrival.

2. display any one of the three components – if you picked the p-arrival on the z-component display that one.

3. Select a time window around the p-arrival by clickingabovethe trace window. The window should be several seconds or tens of seconds before and after the p-arrival. If the 3-comp is a broadband, select a filter first \(Try the 1Hz – 20Hz filter\).

4. select the ‘Azim’ button and select a zoom window around the p-arrival of a few tenths of seconds duration.

5. The 3 components are now displayed in order along with calculated azimuth of arrival, apparent velocity and correlation co-efficient.

6. Repeat this procedure a few times, experimenting with different window lengths and filters. The azimuth should be reasonable, and the correlation coefficient should be as high as possible and positive. Sometimes the correlation coefficient cannot be made positive, despite heroic efforts. The ‘vel’ \(apparent velocity\) will usually be unrealistic. To refresh the screen between attempts, select the ‘plot’ button.

7.  When you are satisfied with the azimuth, save it to the s-file by associating it with a phase. The usual way to do this is to pick an I or E phase \(type ‘e’ or ‘i’\). That phase must be picked on the single upper trace seen on the same screen.

8. Return to multitrace mode by selecting the ‘other c’ button, and selecting the ‘all’ and ‘ok’ button for all the traces.

9. Select the ‘Locat’ button to locate the event. The command screen appears as the location is calculated, and the results are written to the command window. The waveform plot shows both the manually-determined phases and the calculated phases.

10. If you are locating the event from secondary processing in EEV, after locating the event you must update the s-file to include the location by typing the ‘update’ command at the EEV command prompt. Update will run the location program again and write the results to the s- file.



