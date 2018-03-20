# MULPLT: Trace plotting, phase picking and spectral analysis

_**mulplt**_ 是用於波形瀏覽和資料分析上。 此程序能夠進行波相到時的選取、修正儀器響應、生成Wood-Anderson seismogram 用以確定Ml、確定方位角、進行 spectral analysis和particle motion。

_**mulplt**_ 可以獨立用於波形檢視（以_**mulplt**_命令啟動）或與資料庫指令結合（從_**EEV**_以'_**p**_'或'_**po**_'啟動）。

_**mulplt**_可使用指令如下：

```
Channel selection: In multitrace mode, one or several channels can be selected by clicking on the station code. 
Zooming: Select a window with the mouse.
a: Read amplitude.
A: Automatic amplitude reading
b: Filter 5-10 hz
B: Back: Go back one trace in single trace mode
         From eev, multi: Go back one event
         Continous data base: Go back one window
c: Read coda
C: Read end of coda automatically
d: Delete phase.
d: Del W: Delete waveform file(s)
          from EEV, only file names in S-file are deleted.
D: Del S: Delete S-file
          from EEV, multi mode
e: Phase E
E: Call external program
f: Next: Single: Go to next channel
         Multi, One event: Go to next event
         multi, continous data base: Go to next window
F: FK:   FK analysis of array data
g: Groun: Make a ground motion seismogram(s).
h: Azim:  Make 3 component analysis (single mode ONLY) to determine azimuth of arrival.
i:
 Phase I
I: Iasp: Calculate IASPEI synthetic arrival times, which are then
displayed, multitrace only.
j: mb: Generate a synthetic SP seismogram for reading amplitudes
for determining mb.
J: mB:
 Generate a synthetic BB velocity seismogram for reading
amplitudes for determining mB.
k: Ms:
 Generate a synthetic LP seismogram for reading amplitudes
for determining Ms.
K: MS: Generate a synthetic BB velocity seismogram for reading
amplitudes for determining MS.
l: Locat: Locate event, only multi trace mode
m: Filter 15-24 hz
M: Merge: Merge waveform file, mulplt called from EEV, only if files are In working directory.
n: Filter 10- 15 hz
N: Toggle multiple windows to show all traces in one screen or one of the multiple windows.

o: Oth C: Select other channels

O: Out:   Makes an output waveform file of current data on screen. Only multi mode.
p: Regis: PUT (Register) event in database
P: PartM  Particle motion plot, requires the three components in
 multi trace plot
q: Quit:  Quit program
r: Plot:  Replot same event
R: Change radius from epicenter
s: Spec
: Make a spectrum, single mode ONLY.
S:
 Same as s without the noise spectrum, singel trace.
S: Select station for area selection, only multi trace mode.
t: Toggl: Toggle between multi and single mode
T: OutW:  Output file mulplt.wav of what is on screen
u: Same as ’y’ with the difference that all components for all stations are shown.
U: Rotat: Rotate components.
v: Filter 1-5 Hz
y: AllC:  Toggle to and from all channel mode.
Y:
 Pick a theoretical phase if displayed.
w: WA: Remove system response and display synthetic
 Wood-Anderson ground motion in nanometers (nm)
 on next plot (using R or zoom).
W: Oth W: Select other waveform file
z:
 Filter 0.001 to 0.1 Hz
x:
 Filter 0.1 to 1.0 Hz
Z: <W>
 Increase window length in plotting from a continous data base
X: >W< Decrease window lenght when plotting from a continous data base       
>: Print: Will make a hardcopy of all channels of current event with
 the last selected filter, only in multitrace mode.
<: Same as D
*: Scale: Fixed scaling of trace amplitudes.

Up and down arrows: Increase and decrease amplitude
Horizontal arrows: Scroll
_: Dist:  Select plotting channels in distance order.
:  Resp:  Plot response file, single trace mode only.
TAB: NextW: Next window if multiple windows

.: Filt: Variable filter, question of filter limits is given in text
 window.

,: FixF  Fix filter. If pressed aftrer selecting as filter, the filter
 remains fixed until pressing ’,’ again.
’: Variable filter also with number of poles

```



