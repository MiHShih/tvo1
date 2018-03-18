# Plotting of travel times

From EEV use option ‘ttplot’ to generate travel time plot. The program displays P and S travel times as a function of distance and can be used to identify picks that don’t fit. The theoretical travel times are indicated on the plot .



Program to plot observed and calculated travel times \(Figure 6.44 \). The input to the program is an s-file, which has an indicator to a model file \(STATION?.HYP\) and the travel time observations. The program is started by ‘ttplot&lt;sfile-name&gt;’. At the start, TTPLOT relocates the event and calculates distances using the HYPOCENTER program. It then plots all observations with a ‘+’ symbol and the theoretical travel times that are calculated by the program for the first P and S arrivals with solid lines. The program can be useful in routine processing to visualize large residuals, which otherwise are seen from the location program output. The program can also be started from EEV using option ‘ttplot’. It is possible to click on symbols, which will bring up station code, phase, observed travel time and residual on the rigth. The output files are:

ttplot.out- gives station code, phase name, distance, observed travel times and residual.ttplot.eps- Postscript version of plot.

![](/assets/Screen Shot 2018-03-18 at 2.40.33 PM.png)

